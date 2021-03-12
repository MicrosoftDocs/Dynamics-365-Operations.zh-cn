---
title: 内容块模块
description: 此主题介绍内容块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6359c915d053bb00c969b166325f675c0003ead
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980349"
---
# <a name="content-block-module"></a><span data-ttu-id="14e7d-103">内容块模块</span><span class="sxs-lookup"><span data-stu-id="14e7d-103">Content block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="14e7d-104">此主题介绍内容块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="14e7d-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="14e7d-105">概览</span><span class="sxs-lookup"><span data-stu-id="14e7d-105">Overview</span></span>

<span data-ttu-id="14e7d-106">内容块模块用于通过图像和文本的组合营销产品或促销。</span><span class="sxs-lookup"><span data-stu-id="14e7d-106">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="14e7d-107">例如，零售商可向电子商务站点的主页添加一个内容块模块来促销新产品和吸引客户的注意。</span><span class="sxs-lookup"><span data-stu-id="14e7d-107">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="14e7d-108">内容块模块由内容管理系统 (CMS) 的数据驱动。</span><span class="sxs-lookup"><span data-stu-id="14e7d-108">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="14e7d-109">它是不依赖于页面上的其他任何模块的独立模块。</span><span class="sxs-lookup"><span data-stu-id="14e7d-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="14e7d-110">可将内容块模块放到零售商要进行营销或推广（如产品、销售或特色）的任何站点页中。</span><span class="sxs-lookup"><span data-stu-id="14e7d-110">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="14e7d-111">电子商务中的内容块模块示例</span><span class="sxs-lookup"><span data-stu-id="14e7d-111">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="14e7d-112">可在电子商务站点的主页中使用内容块模块来重点展示促销和新产品。</span><span class="sxs-lookup"><span data-stu-id="14e7d-112">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="14e7d-113">可在产品详细信息页上使用内容块模块来展示产品信息。</span><span class="sxs-lookup"><span data-stu-id="14e7d-113">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="14e7d-114">可在一个传送模块中放置多个内容块模块来重点展示多个产品或促销。</span><span class="sxs-lookup"><span data-stu-id="14e7d-114">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="14e7d-115">内容块模块和主题</span><span class="sxs-lookup"><span data-stu-id="14e7d-115">Content block modules and themes</span></span>

<span data-ttu-id="14e7d-116">内容块模块可以支持基于主题的各种布局和样式。</span><span class="sxs-lookup"><span data-stu-id="14e7d-116">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="14e7d-117">例如，Fabrikam 主题支持内容块模块的三种布局变体：主图、特色和磁贴。</span><span class="sxs-lookup"><span data-stu-id="14e7d-117">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="14e7d-118">主图布局在背景上显示带有文字叠加层的图像。</span><span class="sxs-lookup"><span data-stu-id="14e7d-118">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="14e7d-119">功能布局并排显示图像和文本。</span><span class="sxs-lookup"><span data-stu-id="14e7d-119">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="14e7d-120">磁贴布局允许以磁贴格式显示多个内容块。</span><span class="sxs-lookup"><span data-stu-id="14e7d-120">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="14e7d-121">此外，主题可以为每个布局公开不同的属性。</span><span class="sxs-lookup"><span data-stu-id="14e7d-121">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="14e7d-122">主题开发人员可以使用内容块模块构建具有更多样式的更多布局。</span><span class="sxs-lookup"><span data-stu-id="14e7d-122">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="14e7d-123">下图显示了具有主图布局的内容块模块的示例。</span><span class="sxs-lookup"><span data-stu-id="14e7d-123">The following image shows an example of a content block module with a hero layout.</span></span>

![主图模块的示例](./media/Hero.PNG)

<span data-ttu-id="14e7d-125">下图显示了具有特色布局的内容块模块的示例。</span><span class="sxs-lookup"><span data-stu-id="14e7d-125">The following image shows an example of a content block module with a feature layout.</span></span>

![特色模块示例](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="14e7d-127">内容块模块属性</span><span class="sxs-lookup"><span data-stu-id="14e7d-127">Content block module properties</span></span>

| <span data-ttu-id="14e7d-128">属性名称</span><span class="sxs-lookup"><span data-stu-id="14e7d-128">Property name</span></span>  | <span data-ttu-id="14e7d-129">值</span><span class="sxs-lookup"><span data-stu-id="14e7d-129">Values</span></span> | <span data-ttu-id="14e7d-130">说明</span><span class="sxs-lookup"><span data-stu-id="14e7d-130">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="14e7d-131">头像</span><span class="sxs-lookup"><span data-stu-id="14e7d-131">Image</span></span>          | <span data-ttu-id="14e7d-132">图像文件</span><span class="sxs-lookup"><span data-stu-id="14e7d-132">Image file</span></span> | <span data-ttu-id="14e7d-133">可使用图像来展示产品或促销。</span><span class="sxs-lookup"><span data-stu-id="14e7d-133">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="14e7d-134">可将图像上传到图像库，也可以使用现有图像。</span><span class="sxs-lookup"><span data-stu-id="14e7d-134">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="14e7d-135">标题</span><span class="sxs-lookup"><span data-stu-id="14e7d-135">Heading</span></span>        | <span data-ttu-id="14e7d-136">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="14e7d-136">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="14e7d-137">每个主图模块都有标题。</span><span class="sxs-lookup"><span data-stu-id="14e7d-137">Every hero module can have a heading.</span></span> <span data-ttu-id="14e7d-138">默认情况下，将 **H2** 标题标记用于标题。</span><span class="sxs-lookup"><span data-stu-id="14e7d-138">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="14e7d-139">但是，可更改此标记以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="14e7d-139">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="14e7d-140">段落</span><span class="sxs-lookup"><span data-stu-id="14e7d-140">Paragraph</span></span>      | <span data-ttu-id="14e7d-141">段落文本</span><span class="sxs-lookup"><span data-stu-id="14e7d-141">Paragraph text</span></span> | <span data-ttu-id="14e7d-142">主图模块支持富文本格式的段落文本。</span><span class="sxs-lookup"><span data-stu-id="14e7d-142">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="14e7d-143">支持某些基本的富文本功能，如加粗，加下划线、斜体文本和超链接。</span><span class="sxs-lookup"><span data-stu-id="14e7d-143">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="14e7d-144">为模块应用的页面主题可替代这些功能中的一部分。</span><span class="sxs-lookup"><span data-stu-id="14e7d-144">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="14e7d-145">链接</span><span class="sxs-lookup"><span data-stu-id="14e7d-145">Link</span></span>           | <span data-ttu-id="14e7d-146">链接文本、链接 URL、可访问丰富 Internet 应用程序 (ARIA) 标签和 **在新标签页中打开链接**</span><span class="sxs-lookup"><span data-stu-id="14e7d-146">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="14e7d-147">主图模块支持一个或多个“调用操作”链接。</span><span class="sxs-lookup"><span data-stu-id="14e7d-147">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="14e7d-148">如果添加链接，则需要链接文本、URL 和 ARIA 标签。</span><span class="sxs-lookup"><span data-stu-id="14e7d-148">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="14e7d-149">ARIA 标签应该具有描述性，以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="14e7d-149">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="14e7d-150">可将链接配置为在新标签页中打开。</span><span class="sxs-lookup"><span data-stu-id="14e7d-150">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="14e7d-151">Fabrikam 主题公开的内容块模块属性</span><span class="sxs-lookup"><span data-stu-id="14e7d-151">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="14e7d-152">属性名称</span><span class="sxs-lookup"><span data-stu-id="14e7d-152">Property name</span></span>  | <span data-ttu-id="14e7d-153">值</span><span class="sxs-lookup"><span data-stu-id="14e7d-153">Values</span></span> | <span data-ttu-id="14e7d-154">说明</span><span class="sxs-lookup"><span data-stu-id="14e7d-154">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="14e7d-155">文本放置</span><span class="sxs-lookup"><span data-stu-id="14e7d-155">Text placement</span></span> | <span data-ttu-id="14e7d-156">**向左对齐**、**向右对齐**、**居中对齐**</span><span class="sxs-lookup"><span data-stu-id="14e7d-156">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="14e7d-157">此属性定义文本在图像上的位置。</span><span class="sxs-lookup"><span data-stu-id="14e7d-157">This property defines the position of the text on the image.</span></span> <span data-ttu-id="14e7d-158">它仅适用于主图布局。</span><span class="sxs-lookup"><span data-stu-id="14e7d-158">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="14e7d-159">文本主题</span><span class="sxs-lookup"><span data-stu-id="14e7d-159">Text theme</span></span>     | <span data-ttu-id="14e7d-160">**浅** 或 **深**</span><span class="sxs-lookup"><span data-stu-id="14e7d-160">**Light** or **Dark**</span></span> | <span data-ttu-id="14e7d-161">可以基于背景图像为文本定义颜色主题。</span><span class="sxs-lookup"><span data-stu-id="14e7d-161">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="14e7d-162">例如，如果图像采用了深色背景，则可应用浅色主题来凸显文本和加强颜色对比度，以达到辅助功能目的。</span><span class="sxs-lookup"><span data-stu-id="14e7d-162">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="14e7d-163">它仅适用于主图布局。</span><span class="sxs-lookup"><span data-stu-id="14e7d-163">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="14e7d-164">图像放置</span><span class="sxs-lookup"><span data-stu-id="14e7d-164">Image placement</span></span>       | <span data-ttu-id="14e7d-165">**向左对齐**、**向右对齐**</span><span class="sxs-lookup"><span data-stu-id="14e7d-165">**Left**,  **Right**</span></span> | <span data-ttu-id="14e7d-166">此属性指定图像应位于文本的左侧还是右侧。</span><span class="sxs-lookup"><span data-stu-id="14e7d-166">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="14e7d-167">它仅适用于特色布局。</span><span class="sxs-lookup"><span data-stu-id="14e7d-167">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="14e7d-168">向新页面添加内容块模块</span><span class="sxs-lookup"><span data-stu-id="14e7d-168">Add a content block module to a new page</span></span>

<span data-ttu-id="14e7d-169">若要向新页面添加主图模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="14e7d-169">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="14e7d-170">转到 **模板**，然后创建一个名称为 **内容块模板** 的页面模板。</span><span class="sxs-lookup"><span data-stu-id="14e7d-170">Go to **Templates**, and create a page template that is named **Content block template**.</span></span>
1. <span data-ttu-id="14e7d-171">在默认页的 **主** 插槽中，添加一个主图模块。</span><span class="sxs-lookup"><span data-stu-id="14e7d-171">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="14e7d-172">选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="14e7d-172">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="14e7d-173">使用您刚才创建的主图模板创建一个名称为 **内容块页** 的页面。</span><span class="sxs-lookup"><span data-stu-id="14e7d-173">Use the hero template that you just created to create a page that is named **Content block page**.</span></span>
1. <span data-ttu-id="14e7d-174">在默认页的 **主** 插槽，选择省略号按钮 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="14e7d-174">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="14e7d-175">在 **添加模块** 对话框中 **选择模块** 下，选择主图模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="14e7d-175">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="14e7d-176">在左侧的大纲树中，选择该内容块模块。</span><span class="sxs-lookup"><span data-stu-id="14e7d-176">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="14e7d-177">在右侧的属性窗格中，选择 **添加图像**。</span><span class="sxs-lookup"><span data-stu-id="14e7d-177">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="14e7d-178">然后选择现有图像或上传新图像。</span><span class="sxs-lookup"><span data-stu-id="14e7d-178">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="14e7d-179">选择 **标题**。</span><span class="sxs-lookup"><span data-stu-id="14e7d-179">Select **Heading**.</span></span>
1. <span data-ttu-id="14e7d-180">在 **标题** 对话框中，添加标题文本，选择标题级别，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="14e7d-180">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="14e7d-181">在 **富文本** 下，根据需要添加文本。</span><span class="sxs-lookup"><span data-stu-id="14e7d-181">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="14e7d-182">选择 **添加链接**。</span><span class="sxs-lookup"><span data-stu-id="14e7d-182">Select **Add Link**.</span></span>
1. <span data-ttu-id="14e7d-183">在 **链接** 对话框中，添加链接的链接文本、链接 URL 和 ARIA 标签，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="14e7d-183">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="14e7d-184">选择 **主图** 布局。</span><span class="sxs-lookup"><span data-stu-id="14e7d-184">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="14e7d-185">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="14e7d-185">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="14e7d-186">选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="14e7d-186">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="14e7d-187">其他资源</span><span class="sxs-lookup"><span data-stu-id="14e7d-187">Additional resources</span></span>

[<span data-ttu-id="14e7d-188">模块库概述</span><span class="sxs-lookup"><span data-stu-id="14e7d-188">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="14e7d-189">促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="14e7d-189">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="14e7d-190">传送模块</span><span class="sxs-lookup"><span data-stu-id="14e7d-190">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="14e7d-191">文本块模块</span><span class="sxs-lookup"><span data-stu-id="14e7d-191">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="14e7d-192">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="14e7d-192">Video player module</span></span>](add-video-player.md)
