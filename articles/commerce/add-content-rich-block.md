---
title: 内容丰富块模块
description: 此主题介绍内容丰富块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785413"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="80292-103">内容丰富块模块</span><span class="sxs-lookup"><span data-stu-id="80292-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="80292-104">此主题介绍内容丰富块模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="80292-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="80292-105">概览</span><span class="sxs-lookup"><span data-stu-id="80292-105">Overview</span></span>

<span data-ttu-id="80292-106">内容丰富块模块是可在其中放入一个或多个内容丰富块项的特殊容器。</span><span class="sxs-lookup"><span data-stu-id="80292-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="80292-107">内容丰富块模块用于页面中的文本内容。</span><span class="sxs-lookup"><span data-stu-id="80292-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="80292-108">此内容可以是参考内容或促销内容。</span><span class="sxs-lookup"><span data-stu-id="80292-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="80292-109">内容丰富块模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。</span><span class="sxs-lookup"><span data-stu-id="80292-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="80292-110">它们是不依赖于页面上下文或其他任何模块的独立模块。</span><span class="sxs-lookup"><span data-stu-id="80292-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="80292-111">电子商务中的内容丰富块模块示例</span><span class="sxs-lookup"><span data-stu-id="80292-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="80292-112">可通过以下方式使用内容丰富块模块：</span><span class="sxs-lookup"><span data-stu-id="80292-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="80292-113">在产品详细信息页中展示产品特色。</span><span class="sxs-lookup"><span data-stu-id="80292-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="80292-114">任何页面中起到参考作用。</span><span class="sxs-lookup"><span data-stu-id="80292-114">For informational purposes on any page.</span></span> <span data-ttu-id="80292-115">例如，其可介绍会员计划的优点，描述装运和退货政策，解答常见问题或提供“关于我们”内容。</span><span class="sxs-lookup"><span data-stu-id="80292-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="80292-116">在产品详细信息页中添加自定义消息。</span><span class="sxs-lookup"><span data-stu-id="80292-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="80292-117">（例如，“订单金额超过 50 美元免运费”）。</span><span class="sxs-lookup"><span data-stu-id="80292-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="80292-118">产品详细信息页、购物车页、结帐页和其他页上的免责声明和联系详细信息（例如，“装运和退货政策应遵守商店政策”）。</span><span class="sxs-lookup"><span data-stu-id="80292-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="80292-119">内容丰富块模块属性</span><span class="sxs-lookup"><span data-stu-id="80292-119">Content rich block module properties</span></span>

| <span data-ttu-id="80292-120">属性名称</span><span class="sxs-lookup"><span data-stu-id="80292-120">Property name</span></span>     | <span data-ttu-id="80292-121">值</span><span class="sxs-lookup"><span data-stu-id="80292-121">Value</span></span>                                 | <span data-ttu-id="80292-122">属性</span><span class="sxs-lookup"><span data-stu-id="80292-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="80292-123">列数</span><span class="sxs-lookup"><span data-stu-id="80292-123">Number of columns</span></span> | <span data-ttu-id="80292-124">从 **1** 到 **4** 的数字</span><span class="sxs-lookup"><span data-stu-id="80292-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="80292-125">内容丰富块中的列数。</span><span class="sxs-lookup"><span data-stu-id="80292-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="80292-126">最多四列。</span><span class="sxs-lookup"><span data-stu-id="80292-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="80292-127">宽度</span><span class="sxs-lookup"><span data-stu-id="80292-127">Width</span></span>             | <span data-ttu-id="80292-128">**充满容器**或**充满屏幕**</span><span class="sxs-lookup"><span data-stu-id="80292-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="80292-129">如果此值设置为**充满容器**，则容器内的项的宽度限制为容器的宽度。</span><span class="sxs-lookup"><span data-stu-id="80292-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="80292-130">如果此值设置为**充满屏幕**，则商品不限制为容器宽度，而是可以进入全屏模式。</span><span class="sxs-lookup"><span data-stu-id="80292-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="80292-131">可以更改此值以获得所需布局。</span><span class="sxs-lookup"><span data-stu-id="80292-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="80292-132">内容丰富块项模块属性</span><span class="sxs-lookup"><span data-stu-id="80292-132">Content rich block item module properties</span></span>

| <span data-ttu-id="80292-133">属性名称</span><span class="sxs-lookup"><span data-stu-id="80292-133">Property name</span></span> | <span data-ttu-id="80292-134">值</span><span class="sxs-lookup"><span data-stu-id="80292-134">Value</span></span>          | <span data-ttu-id="80292-135">说明</span><span class="sxs-lookup"><span data-stu-id="80292-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="80292-136">段落</span><span class="sxs-lookup"><span data-stu-id="80292-136">Paragraph</span></span>     | <span data-ttu-id="80292-137">段落文本</span><span class="sxs-lookup"><span data-stu-id="80292-137">Paragraph text</span></span> | <span data-ttu-id="80292-138">每个内容丰富块项随附的文本。</span><span class="sxs-lookup"><span data-stu-id="80292-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="80292-139">支持某些基本的富文本功能，如加粗，加下划线和斜体文本。</span><span class="sxs-lookup"><span data-stu-id="80292-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="80292-140">向页面添加内容丰富块模块</span><span class="sxs-lookup"><span data-stu-id="80292-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="80292-141">若要向新页面添加内容丰富块模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="80292-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="80292-142">创建一个名称为**内容模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="80292-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="80292-143">在默认页的**主**插槽中，添加一个内容丰富块模块。</span><span class="sxs-lookup"><span data-stu-id="80292-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="80292-144">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="80292-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="80292-145">使用您刚才创建的内容模板创建一个名称为**内容页**的页面。</span><span class="sxs-lookup"><span data-stu-id="80292-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="80292-146">在新页的**主**插槽中，添加一个内容丰富块模块。</span><span class="sxs-lookup"><span data-stu-id="80292-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="80292-147">在内容丰富块模块的属性中，将列数设置为 **2**。</span><span class="sxs-lookup"><span data-stu-id="80292-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="80292-148">在内容丰富块模块中，选择**添加模块**，然后添加一个内容丰富块项（例如，**item1**）。</span><span class="sxs-lookup"><span data-stu-id="80292-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="80292-149">在新内容丰富块项中，添加段落文本。</span><span class="sxs-lookup"><span data-stu-id="80292-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="80292-150">在内容丰富块模块中，选择**添加模块**，然后添加一个内容丰富块项（例如，**item2**）。</span><span class="sxs-lookup"><span data-stu-id="80292-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="80292-151">在新内容丰富块项中，添加段落文本。</span><span class="sxs-lookup"><span data-stu-id="80292-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="80292-152">保存页面，然后预览更改。</span><span class="sxs-lookup"><span data-stu-id="80292-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="80292-153">应该可以在两列视图中看到两个富文本块。</span><span class="sxs-lookup"><span data-stu-id="80292-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="80292-154">签入页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="80292-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="80292-155">如果添加第三个内容丰富块项，将把该项堆叠在之前添加的两个项的下方。</span><span class="sxs-lookup"><span data-stu-id="80292-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="80292-156">可通过更改容器中的列和项的数量为文本内容获得不同布局。</span><span class="sxs-lookup"><span data-stu-id="80292-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80292-157">其他资源</span><span class="sxs-lookup"><span data-stu-id="80292-157">Additional resources</span></span>

[<span data-ttu-id="80292-158">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="80292-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="80292-159">预警模块</span><span class="sxs-lookup"><span data-stu-id="80292-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="80292-160">传送模块</span><span class="sxs-lookup"><span data-stu-id="80292-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="80292-161">内容放置模块</span><span class="sxs-lookup"><span data-stu-id="80292-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="80292-162">特色模块</span><span class="sxs-lookup"><span data-stu-id="80292-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="80292-163">主图模块</span><span class="sxs-lookup"><span data-stu-id="80292-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="80292-164">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="80292-164">Video player module</span></span>](add-video-player.md)

