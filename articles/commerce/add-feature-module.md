---
title: 特色模块
description: 此主题介绍特色模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785275"
---
# <a name="feature-module"></a><span data-ttu-id="0ce22-103">特色模块</span><span class="sxs-lookup"><span data-stu-id="0ce22-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0ce22-104">此主题介绍特色模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="0ce22-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0ce22-105">概览</span><span class="sxs-lookup"><span data-stu-id="0ce22-105">Overview</span></span>

<span data-ttu-id="0ce22-106">特色模块用于通过图像和文本的组合营销产品或促销。</span><span class="sxs-lookup"><span data-stu-id="0ce22-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="0ce22-107">例如，零售商可以向产品详细信息页添加特色模块以重点介绍产品的特色。</span><span class="sxs-lookup"><span data-stu-id="0ce22-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="0ce22-108">特色模块由内容管理系统 (CMS) 的数据驱动。</span><span class="sxs-lookup"><span data-stu-id="0ce22-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="0ce22-109">它是不依赖于页面上的其他任何模块的独立模块。</span><span class="sxs-lookup"><span data-stu-id="0ce22-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="0ce22-110">可将特色模块放到零售商要进行营销或推广（如产品、销售或特色）的任何站点页中。</span><span class="sxs-lookup"><span data-stu-id="0ce22-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="0ce22-111">电子商务中的特色模块示例</span><span class="sxs-lookup"><span data-stu-id="0ce22-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="0ce22-112">可在以下页中使用特色模块：</span><span class="sxs-lookup"><span data-stu-id="0ce22-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="0ce22-113">产品详细信息页，用于展示产品特色</span><span class="sxs-lookup"><span data-stu-id="0ce22-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="0ce22-114">主页，用于促销产品</span><span class="sxs-lookup"><span data-stu-id="0ce22-114">The home page, to promote products</span></span>
- <span data-ttu-id="0ce22-115">类别页，用于重点展示一类产品</span><span class="sxs-lookup"><span data-stu-id="0ce22-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="0ce22-116">特色模块属性</span><span class="sxs-lookup"><span data-stu-id="0ce22-116">Feature module properties</span></span>

| <span data-ttu-id="0ce22-117">属性名称</span><span class="sxs-lookup"><span data-stu-id="0ce22-117">Property name</span></span>     | <span data-ttu-id="0ce22-118">值</span><span class="sxs-lookup"><span data-stu-id="0ce22-118">Values</span></span> | <span data-ttu-id="0ce22-119">说明</span><span class="sxs-lookup"><span data-stu-id="0ce22-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="0ce22-120">头像</span><span class="sxs-lookup"><span data-stu-id="0ce22-120">Image</span></span>             | <span data-ttu-id="0ce22-121">图像文件</span><span class="sxs-lookup"><span data-stu-id="0ce22-121">Image file</span></span> | <span data-ttu-id="0ce22-122">可使用图像来营销产品或促销。</span><span class="sxs-lookup"><span data-stu-id="0ce22-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="0ce22-123">可将图像上传到图像库，也可以使用现有图像。</span><span class="sxs-lookup"><span data-stu-id="0ce22-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="0ce22-124">标题</span><span class="sxs-lookup"><span data-stu-id="0ce22-124">Heading</span></span>           | <span data-ttu-id="0ce22-125">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="0ce22-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="0ce22-126">每个特色模块都有标题。</span><span class="sxs-lookup"><span data-stu-id="0ce22-126">Every feature module can have a heading.</span></span> <span data-ttu-id="0ce22-127">默认情况下，将 **H2** 标题标记用于标题。</span><span class="sxs-lookup"><span data-stu-id="0ce22-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="0ce22-128">但是，可更改此标记以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="0ce22-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="0ce22-129">段落</span><span class="sxs-lookup"><span data-stu-id="0ce22-129">Paragraph</span></span>         | <span data-ttu-id="0ce22-130">段落文本</span><span class="sxs-lookup"><span data-stu-id="0ce22-130">Paragraph text</span></span> | <span data-ttu-id="0ce22-131">特色模块支持富文本格式的段落文本。</span><span class="sxs-lookup"><span data-stu-id="0ce22-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="0ce22-132">支持某些基本的富文本功能，如加粗，加下划线、斜体文本和超链接。</span><span class="sxs-lookup"><span data-stu-id="0ce22-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="0ce22-133">为模块应用的页面主题可替代这些功能中的一部分。</span><span class="sxs-lookup"><span data-stu-id="0ce22-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="0ce22-134">链接</span><span class="sxs-lookup"><span data-stu-id="0ce22-134">Link</span></span>              | <span data-ttu-id="0ce22-135">链接文本、链接 URL、可访问丰富 Internet 应用程序 (ARIA) 标签和**在新标签页中打开链接**</span><span class="sxs-lookup"><span data-stu-id="0ce22-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="0ce22-136">特色模块支持一个或多个“调用操作”链接。</span><span class="sxs-lookup"><span data-stu-id="0ce22-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="0ce22-137">如果添加链接，则需要链接文本、URL 和 ARIA 标签。</span><span class="sxs-lookup"><span data-stu-id="0ce22-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="0ce22-138">ARIA 标签应该具有描述性，以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="0ce22-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="0ce22-139">可将链接配置为在新标签页中打开。</span><span class="sxs-lookup"><span data-stu-id="0ce22-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="0ce22-140">图像放置</span><span class="sxs-lookup"><span data-stu-id="0ce22-140">Image placement</span></span>   | <span data-ttu-id="0ce22-141">**靠右**、**靠左**、**靠上**或**靠下**</span><span class="sxs-lookup"><span data-stu-id="0ce22-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="0ce22-142">此属性定义图像相对文本的位置。</span><span class="sxs-lookup"><span data-stu-id="0ce22-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="0ce22-143">例如，如果选择**靠右**，则图像在文本右侧显示。</span><span class="sxs-lookup"><span data-stu-id="0ce22-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="0ce22-144">图像列大小</span><span class="sxs-lookup"><span data-stu-id="0ce22-144">Image column size</span></span> | <span data-ttu-id="0ce22-145">从 **1** 到 **12** 的值</span><span class="sxs-lookup"><span data-stu-id="0ce22-145">A value from **1** through **12**</span></span> | <span data-ttu-id="0ce22-146">此属性定义图像相对文本的大小。</span><span class="sxs-lookup"><span data-stu-id="0ce22-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="0ce22-147">大小表示为页面中的列数。</span><span class="sxs-lookup"><span data-stu-id="0ce22-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="0ce22-148">页面中有 12 列。</span><span class="sxs-lookup"><span data-stu-id="0ce22-148">There are 12 columns on a page.</span></span> <span data-ttu-id="0ce22-149">默认情况下，图像和文本的大小相等（分别六列）。</span><span class="sxs-lookup"><span data-stu-id="0ce22-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="0ce22-150">但是，可以根据需要调整大小。</span><span class="sxs-lookup"><span data-stu-id="0ce22-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="0ce22-151">向新页添加特色模块</span><span class="sxs-lookup"><span data-stu-id="0ce22-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="0ce22-152">若要向新页面添加特色模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="0ce22-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0ce22-153">转到**模板**，然后创建一个名称为**特色模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="0ce22-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="0ce22-154">在默认页的**主**插槽中，添加一个特色模块。</span><span class="sxs-lookup"><span data-stu-id="0ce22-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="0ce22-155">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="0ce22-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="0ce22-156">使用您刚才创建的特色模板创建一个名称为**特色页**的页面。</span><span class="sxs-lookup"><span data-stu-id="0ce22-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="0ce22-157">在默认页的**主**插槽，选择省略号按钮 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="0ce22-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0ce22-158">在**添加模块**对话框中**选择模块**下，选择一个特色模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0ce22-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="0ce22-159">在左侧的大纲树中，选择该特色模块。</span><span class="sxs-lookup"><span data-stu-id="0ce22-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="0ce22-160">在右侧的属性窗格中，选择**添加图像**。</span><span class="sxs-lookup"><span data-stu-id="0ce22-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="0ce22-161">然后选择现有图像或上传新图像。</span><span class="sxs-lookup"><span data-stu-id="0ce22-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="0ce22-162">选择**标题**。</span><span class="sxs-lookup"><span data-stu-id="0ce22-162">Select **Heading**.</span></span>
1. <span data-ttu-id="0ce22-163">在**标题**对话框中，添加标题文本，选择标题级别，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0ce22-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="0ce22-164">在**富文本**下，根据需要添加文本。</span><span class="sxs-lookup"><span data-stu-id="0ce22-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="0ce22-165">选择**添加操作链接**。</span><span class="sxs-lookup"><span data-stu-id="0ce22-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="0ce22-166">在**操作链接**对话框中，添加链接的链接文本、链接 URL 和 ARIA 标签，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0ce22-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="0ce22-167">保存页面，然后预览更改。</span><span class="sxs-lookup"><span data-stu-id="0ce22-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="0ce22-168">签入页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="0ce22-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ce22-169">其他资源</span><span class="sxs-lookup"><span data-stu-id="0ce22-169">Additional resources</span></span>

[<span data-ttu-id="0ce22-170">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="0ce22-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0ce22-171">预警模块</span><span class="sxs-lookup"><span data-stu-id="0ce22-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="0ce22-172">传送模块</span><span class="sxs-lookup"><span data-stu-id="0ce22-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="0ce22-173">内容丰富块模块</span><span class="sxs-lookup"><span data-stu-id="0ce22-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="0ce22-174">内容放置模块</span><span class="sxs-lookup"><span data-stu-id="0ce22-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="0ce22-175">主图模块</span><span class="sxs-lookup"><span data-stu-id="0ce22-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="0ce22-176">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="0ce22-176">Video player module</span></span>](add-video-player.md)
