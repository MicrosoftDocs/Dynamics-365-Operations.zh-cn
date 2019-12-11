---
title: 内容放置模块
description: 此主题介绍内容放置模块和内容放置项模块，以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785291"
---
# <a name="content-placement-module"></a><span data-ttu-id="d7524-103">内容放置模块</span><span class="sxs-lookup"><span data-stu-id="d7524-103">Content placement module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d7524-104">此主题介绍内容放置模块和内容放置项模块，以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="d7524-104">This topic covers content placement and content placement item modules, and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d7524-105">概览</span><span class="sxs-lookup"><span data-stu-id="d7524-105">Overview</span></span>

<span data-ttu-id="d7524-106">内容放置模块是可以将其他模块按照特定布局放到其中的特殊容器。</span><span class="sxs-lookup"><span data-stu-id="d7524-106">A content placement module is a special container that other modules can be put inside in a specific layout.</span></span> <span data-ttu-id="d7524-107">内容放置模块支持将以下模块类型用作子模块：内容放置项、帐户欢迎项、帐户订单项、帐户愿望列表项和帐户个人资料项。</span><span class="sxs-lookup"><span data-stu-id="d7524-107">Content placement modules support the following types of modules as child modules: content placement item, account welcome item, account order item, account wish list item, and account profile item.</span></span>

<span data-ttu-id="d7524-108">内容放置模块的数据派生自其支持的子模块。</span><span class="sxs-lookup"><span data-stu-id="d7524-108">Content placement modules derive data from the child modules that they support.</span></span> <span data-ttu-id="d7524-109">因此，可以通过多种方法使用内容放置模块，具体取决于向其添加的模块。</span><span class="sxs-lookup"><span data-stu-id="d7524-109">Therefore, content placement modules can be used in various ways, depending on the modules that are added to it.</span></span>

<span data-ttu-id="d7524-110">内容放置模块使用图像和文本展示促销、政策和产品特色。</span><span class="sxs-lookup"><span data-stu-id="d7524-110">Content placement item modules use both images and text to showcase promotions, policies, and product features.</span></span> <span data-ttu-id="d7524-111">例如，可在主页中使用内容放置项模块显示商店政策或装运信息。</span><span class="sxs-lookup"><span data-stu-id="d7524-111">For example, a content placement item module can be used on a home page to show store policies or shipping information.</span></span> <span data-ttu-id="d7524-112">内容放置项模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。</span><span class="sxs-lookup"><span data-stu-id="d7524-112">Content placement item modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="d7524-113">但是，只能在内容放置模块中使用。</span><span class="sxs-lookup"><span data-stu-id="d7524-113">However, they can be used only inside a content placement module.</span></span>

## <a name="examples-of-content-placement-modules-in-e-commerce"></a><span data-ttu-id="d7524-114">电子商务中的内容放置模块示例</span><span class="sxs-lookup"><span data-stu-id="d7524-114">Examples of content placement modules in e-Commerce</span></span>

* <span data-ttu-id="d7524-115">可在主页或市场营销页中使用其中包含内容放置项模块的内容放置模块，以通过图像和文本展示产品特色、促销、商店政策、装运信息和其他信息。</span><span class="sxs-lookup"><span data-stu-id="d7524-115">Content placement modules that contain content placement item modules can be used on a home page or marketing pages to showcase product features, promotions, store policies, shipping information, and other information through both images and text.</span></span>
* <span data-ttu-id="d7524-116">可在产品详细信息页中使用其中包含内容放置项模块的内容放置模块，以展示产品特色。</span><span class="sxs-lookup"><span data-stu-id="d7524-116">Content placement modules that contain content placement item modules can be used on product details pages to showcase product features.</span></span>
* <span data-ttu-id="d7524-117">可在帐户管理页中使用其中包含帐户欢迎项或帐户订单项模块的内容放置模块。</span><span class="sxs-lookup"><span data-stu-id="d7524-117">Content placement modules that contain account welcome item or account order item modules can be used on account management pages.</span></span>

## <a name="content-placement-module-properties"></a><span data-ttu-id="d7524-118">内容放置模块属性</span><span class="sxs-lookup"><span data-stu-id="d7524-118">Content placement module properties</span></span>

| <span data-ttu-id="d7524-119">属性名称</span><span class="sxs-lookup"><span data-stu-id="d7524-119">Property name</span></span> | <span data-ttu-id="d7524-120">值</span><span class="sxs-lookup"><span data-stu-id="d7524-120">Value</span></span> | <span data-ttu-id="d7524-121">说明</span><span class="sxs-lookup"><span data-stu-id="d7524-121">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="d7524-122">宽度</span><span class="sxs-lookup"><span data-stu-id="d7524-122">Width</span></span>         | <span data-ttu-id="d7524-123">**适合容器**或**充满屏幕**</span><span class="sxs-lookup"><span data-stu-id="d7524-123">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="d7524-124">如果此值设置为**适合容器**，则内容放置模块内的项的宽度限制为内容放置模块的宽度。</span><span class="sxs-lookup"><span data-stu-id="d7524-124">If the value is set to **Fit container**, the items inside the content placement module are restricted to the width of the content placement module.</span></span> <span data-ttu-id="d7524-125">如果此值设置为**充满屏幕**，则项不限制为内容放置模块宽度，而是可以进入全屏模式。</span><span class="sxs-lookup"><span data-stu-id="d7524-125">If the value is set to **Fill screen**, the items aren't restricted to the width of the content placement module but can go into full-screen mode.</span></span> |

## <a name="content-placement-item-module-properties"></a><span data-ttu-id="d7524-126">内容放置项模块属性</span><span class="sxs-lookup"><span data-stu-id="d7524-126">Content placement item module properties</span></span>

| <span data-ttu-id="d7524-127">属性名称</span><span class="sxs-lookup"><span data-stu-id="d7524-127">Property name</span></span> | <span data-ttu-id="d7524-128">值</span><span class="sxs-lookup"><span data-stu-id="d7524-128">Value</span></span> | <span data-ttu-id="d7524-129">说明</span><span class="sxs-lookup"><span data-stu-id="d7524-129">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="d7524-130">标题</span><span class="sxs-lookup"><span data-stu-id="d7524-130">Heading</span></span>       | <span data-ttu-id="d7524-131">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="d7524-131">Heading text and heading tags (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="d7524-132">每个内容放置项模块都可以有标题。</span><span class="sxs-lookup"><span data-stu-id="d7524-132">Every content placement item module can have a heading.</span></span> <span data-ttu-id="d7524-133">**标题**属性支持标题标记。</span><span class="sxs-lookup"><span data-stu-id="d7524-133">The **Heading** property supports heading tags.</span></span> <span data-ttu-id="d7524-134">默认情况下使用 **H2** 标题，但是可以根据辅助功能需要更改标题标记。</span><span class="sxs-lookup"><span data-stu-id="d7524-134">By default, the **H2** heading tag is used, but the heading tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="d7524-135">段落</span><span class="sxs-lookup"><span data-stu-id="d7524-135">Paragraph</span></span>     | <span data-ttu-id="d7524-136">段落文本</span><span class="sxs-lookup"><span data-stu-id="d7524-136">Paragraph text</span></span> | <span data-ttu-id="d7524-137">内容放置项模块支持富文本格式的段落文本。</span><span class="sxs-lookup"><span data-stu-id="d7524-137">Content placement item modules support paragraph text in rich text format.</span></span> <span data-ttu-id="d7524-138">支持某些基本的富文本功能，如加粗，加下划线、斜体文本和超链接。</span><span class="sxs-lookup"><span data-stu-id="d7524-138">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="d7524-139">为模块应用的页面主题可替代这些功能中的一部分。</span><span class="sxs-lookup"><span data-stu-id="d7524-139">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="d7524-140">头像</span><span class="sxs-lookup"><span data-stu-id="d7524-140">Image</span></span>         | <span data-ttu-id="d7524-141">图像文件</span><span class="sxs-lookup"><span data-stu-id="d7524-141">Image file</span></span> | <span data-ttu-id="d7524-142">可以将图像与文本关联。</span><span class="sxs-lookup"><span data-stu-id="d7524-142">An image can be associated with the text.</span></span> |
| <span data-ttu-id="d7524-143">链接</span><span class="sxs-lookup"><span data-stu-id="d7524-143">Link</span></span>          | <span data-ttu-id="d7524-144">链接 URL 和链接文本</span><span class="sxs-lookup"><span data-stu-id="d7524-144">Link URL and link text</span></span> | <span data-ttu-id="d7524-145">可以向文本添加链接，以便将用户重定向到特定页。</span><span class="sxs-lookup"><span data-stu-id="d7524-145">A link can be added to the text to redirect users to a specific page.</span></span> |
| <span data-ttu-id="d7524-146">磁贴大小</span><span class="sxs-lookup"><span data-stu-id="d7524-146">Tile size</span></span>     | <span data-ttu-id="d7524-147">从 **1** 到 **12** 的数字</span><span class="sxs-lookup"><span data-stu-id="d7524-147">A number from **1** through **12**</span></span> | <span data-ttu-id="d7524-148">每个内容放置项的此属性定义项在内容放置模块中应该填充的插槽数量。</span><span class="sxs-lookup"><span data-stu-id="d7524-148">For each content placement item, this property defines the number of slots that the item should fill in the content placement module.</span></span> <span data-ttu-id="d7524-149">内容放置模块的最大大小为 12 个插槽。</span><span class="sxs-lookup"><span data-stu-id="d7524-149">The maximum size of the content placement module is 12 slots.</span></span> <span data-ttu-id="d7524-150">如果内容放置模块中的前 *n* 个项的总磁贴大小超过 12 个插槽，则项换行到下一行。</span><span class="sxs-lookup"><span data-stu-id="d7524-150">If the total tile size for the first *n* items in the content placement module exceeds 12 slots, the items are wrapped to the next row.</span></span> |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a><span data-ttu-id="d7524-151">向页面添加一个其中包含一个内容放置项模块的内容放置模块</span><span class="sxs-lookup"><span data-stu-id="d7524-151">Add a content placement module that contains a content placement item module to a page</span></span>

<span data-ttu-id="d7524-152">若要向新页面添加一个其中包含一个内容放置项模块的内容放置模块并设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d7524-152">To add a content placement module that contains a content placement item module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d7524-153">创建一个名称为**内容放置模块**的模板。</span><span class="sxs-lookup"><span data-stu-id="d7524-153">Create a template that is named **content placement template**.</span></span>
1. <span data-ttu-id="d7524-154">在默认页的**主**插槽中，添加一个内容放置模块。</span><span class="sxs-lookup"><span data-stu-id="d7524-154">In the **Main** slot of the default page, add a content placement module.</span></span>
1. <span data-ttu-id="d7524-155">在该内容放置模块中，添加一个内容放置项模块。</span><span class="sxs-lookup"><span data-stu-id="d7524-155">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="d7524-156">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="d7524-156">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="d7524-157">使用您刚才创建的内容放置模板创建一个名称为**内容放置页**的页面。</span><span class="sxs-lookup"><span data-stu-id="d7524-157">Use the content placement template that you just created to create a page that is named **Content placement page**.</span></span>
1. <span data-ttu-id="d7524-158">在新页的**主**插槽中，添加一个内容放置模块。</span><span class="sxs-lookup"><span data-stu-id="d7524-158">In the **Main** slot of the new page, add a content placement module.</span></span>
1. <span data-ttu-id="d7524-159">在该内容放置模块中，添加一个内容放置项模块。</span><span class="sxs-lookup"><span data-stu-id="d7524-159">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="d7524-160">在内容放置项模块的属性窗格中，选择一个图像，添加标题，添加段落，添加链接，设置链接 URL，然后将磁贴大小设置为 **6**。</span><span class="sxs-lookup"><span data-stu-id="d7524-160">In the property pane for the content placement item module, select an image, add a heading, add a paragraph, add a link, set the link URL, and set the tile size to **6**.</span></span>
1. <span data-ttu-id="d7524-161">重复步骤 7 和 8 再添加一个采用相同磁贴大小的内容放置项模块。</span><span class="sxs-lookup"><span data-stu-id="d7524-161">Repeat steps 7 and 8 to add another content placement item module that has the same tile size.</span></span>
1. <span data-ttu-id="d7524-162">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="d7524-162">Save and preview the page.</span></span> <span data-ttu-id="d7524-163">应该会看到两个并排显示的内容放置项。</span><span class="sxs-lookup"><span data-stu-id="d7524-163">You should see two content placement items that appear side by side.</span></span> <span data-ttu-id="d7524-164">可调整每个内容放置项模块的**磁贴大小**属性，或添加更多模块以获得所需布局。</span><span class="sxs-lookup"><span data-stu-id="d7524-164">You can adjust the **Tile size** property of each content placement item module or add more modules to achieve the desired layout.</span></span>
1. <span data-ttu-id="d7524-165">签入页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="d7524-165">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7524-166">其他资源</span><span class="sxs-lookup"><span data-stu-id="d7524-166">Additional resources</span></span>

[<span data-ttu-id="d7524-167">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="d7524-167">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d7524-168">预警模块</span><span class="sxs-lookup"><span data-stu-id="d7524-168">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="d7524-169">传送模块</span><span class="sxs-lookup"><span data-stu-id="d7524-169">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="d7524-170">内容丰富块模块</span><span class="sxs-lookup"><span data-stu-id="d7524-170">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="d7524-171">特色模块</span><span class="sxs-lookup"><span data-stu-id="d7524-171">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="d7524-172">主图模块</span><span class="sxs-lookup"><span data-stu-id="d7524-172">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="d7524-173">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="d7524-173">Video player module</span></span>](add-video-player.md)
