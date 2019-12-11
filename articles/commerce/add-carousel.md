---
title: 传送模块
description: 此主题介绍传送模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785229"
---
# <a name="carousel-module"></a><span data-ttu-id="98205-103">传送模块</span><span class="sxs-lookup"><span data-stu-id="98205-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="98205-104">此主题介绍传送模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="98205-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="98205-105">概览</span><span class="sxs-lookup"><span data-stu-id="98205-105">Overview</span></span>

<span data-ttu-id="98205-106">传送模块用于将多个促销项放到客户可浏览的传送中。</span><span class="sxs-lookup"><span data-stu-id="98205-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="98205-107">这是用于承载其他模块的特殊容器模块。</span><span class="sxs-lookup"><span data-stu-id="98205-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="98205-108">例如，零售商可在主页中使用传送模块展示多个新产品或促销。</span><span class="sxs-lookup"><span data-stu-id="98205-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="98205-109">可以在传送模块中添加主图模块和特色模块。</span><span class="sxs-lookup"><span data-stu-id="98205-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="98205-110">然后，传送模块的属性定义如何显示这些模块。</span><span class="sxs-lookup"><span data-stu-id="98205-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="98205-111">电子商务中的传送模块示例</span><span class="sxs-lookup"><span data-stu-id="98205-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="98205-112">可在主页中使用内部有多个促销模块的传送。</span><span class="sxs-lookup"><span data-stu-id="98205-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="98205-113">可在产品详细信息页中使用内部有多个促销模块的传送。</span><span class="sxs-lookup"><span data-stu-id="98205-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="98205-114">可在任何市场营销页中使用传送来促销多个促销或产品。</span><span class="sxs-lookup"><span data-stu-id="98205-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="98205-115">传送模块属性</span><span class="sxs-lookup"><span data-stu-id="98205-115">Carousel module properties</span></span>

| <span data-ttu-id="98205-116">属性名称</span><span class="sxs-lookup"><span data-stu-id="98205-116">Property name</span></span>             | <span data-ttu-id="98205-117">值</span><span class="sxs-lookup"><span data-stu-id="98205-117">Value</span></span>                                | <span data-ttu-id="98205-118">说明</span><span class="sxs-lookup"><span data-stu-id="98205-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="98205-119">自动播放</span><span class="sxs-lookup"><span data-stu-id="98205-119">Autoplay</span></span>                  | <span data-ttu-id="98205-120">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="98205-120">**True** or **False**</span></span>                | <span data-ttu-id="98205-121">如果此值设置为 **True**，将自动在传送内的项之间进行切换。</span><span class="sxs-lookup"><span data-stu-id="98205-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="98205-122">如果此值设置为 **False**，则除非客户使用键盘或鼠标从一个项移到下一个项，否则不进行切换。</span><span class="sxs-lookup"><span data-stu-id="98205-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="98205-123">幻灯片切换间隔</span><span class="sxs-lookup"><span data-stu-id="98205-123">Slide transition interval</span></span> | <span data-ttu-id="98205-124">以秒为单位的值</span><span class="sxs-lookup"><span data-stu-id="98205-124">A value in seconds</span></span>                   | <span data-ttu-id="98205-125">项之间的切换间隔。</span><span class="sxs-lookup"><span data-stu-id="98205-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="98205-126">切换动画</span><span class="sxs-lookup"><span data-stu-id="98205-126">Transition animation</span></span>      | <span data-ttu-id="98205-127">**幻灯片**或**淡化**</span><span class="sxs-lookup"><span data-stu-id="98205-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="98205-128">切换效果。</span><span class="sxs-lookup"><span data-stu-id="98205-128">The transition effect.</span></span> |
| <span data-ttu-id="98205-129">宽度</span><span class="sxs-lookup"><span data-stu-id="98205-129">Width</span></span>                     | <span data-ttu-id="98205-130">**适合容器**或**充满屏幕**</span><span class="sxs-lookup"><span data-stu-id="98205-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="98205-131">如果此值设置为**适合容器**，则传送内的项的宽度限制为传送的宽度。</span><span class="sxs-lookup"><span data-stu-id="98205-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="98205-132">如果此值设置为**充满屏幕**，则项不限制为传送宽度，而是可以进入全屏模式。</span><span class="sxs-lookup"><span data-stu-id="98205-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="98205-133">可以更改此值以获得所需布局。</span><span class="sxs-lookup"><span data-stu-id="98205-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="98205-134">向页面添加传送模块</span><span class="sxs-lookup"><span data-stu-id="98205-134">Add a carousel module to a page</span></span>

<span data-ttu-id="98205-135">若要向新页面添加传送模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="98205-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="98205-136">创建一个名称为**传送模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="98205-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="98205-137">在默认页的**主**插槽中，添加一个传送模块。</span><span class="sxs-lookup"><span data-stu-id="98205-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="98205-138">向该传送模块添加一个主图模块。</span><span class="sxs-lookup"><span data-stu-id="98205-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="98205-139">向该传送模块添加一个特色模块。</span><span class="sxs-lookup"><span data-stu-id="98205-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="98205-140">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="98205-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="98205-141">使用您刚才创建的传送模板创建一个名称为**传送页**的页面。</span><span class="sxs-lookup"><span data-stu-id="98205-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="98205-142">在新页的**主**插槽中，添加一个传送模块。</span><span class="sxs-lookup"><span data-stu-id="98205-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="98205-143">将该传送模块的**宽度**属性设置为**充满屏幕**。</span><span class="sxs-lookup"><span data-stu-id="98205-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="98205-144">将**切换动画**属性设置为**幻灯片**。</span><span class="sxs-lookup"><span data-stu-id="98205-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="98205-145">向该传送模块添加一个主图模块。</span><span class="sxs-lookup"><span data-stu-id="98205-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="98205-146">在主图模块汇总，添加图像和标题，然后选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="98205-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="98205-147">向该传送模块添加一个特色模块。</span><span class="sxs-lookup"><span data-stu-id="98205-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="98205-148">在特色模块中，添加图像、标题和一段文本。</span><span class="sxs-lookup"><span data-stu-id="98205-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="98205-149">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="98205-149">Save and preview the page.</span></span> <span data-ttu-id="98205-150">此页应该显示一个传送，其中有两个模块（即主图模块和特色模块）。</span><span class="sxs-lookup"><span data-stu-id="98205-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="98205-151">可以更改传送、主图和特色模块的其他属性以获得所需效果。</span><span class="sxs-lookup"><span data-stu-id="98205-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="98205-152">签入页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="98205-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98205-153">其他资源</span><span class="sxs-lookup"><span data-stu-id="98205-153">Additional resources</span></span>

[<span data-ttu-id="98205-154">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="98205-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="98205-155">预警模块</span><span class="sxs-lookup"><span data-stu-id="98205-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="98205-156">内容丰富块模块</span><span class="sxs-lookup"><span data-stu-id="98205-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="98205-157">内容放置模块</span><span class="sxs-lookup"><span data-stu-id="98205-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="98205-158">特色模块</span><span class="sxs-lookup"><span data-stu-id="98205-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="98205-159">主图模块</span><span class="sxs-lookup"><span data-stu-id="98205-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="98205-160">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="98205-160">Video player module</span></span>](add-video-player.md)
