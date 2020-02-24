---
title: 传送模块
description: 此主题介绍传送模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025773"
---
# <a name="carousel-module"></a><span data-ttu-id="c088e-103">传送模块</span><span class="sxs-lookup"><span data-stu-id="c088e-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c088e-104">此主题介绍传送模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="c088e-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c088e-105">概览</span><span class="sxs-lookup"><span data-stu-id="c088e-105">Overview</span></span>

<span data-ttu-id="c088e-106">传送模块用于将多个促销项（包括大量图像）放到客户可浏览的旋转式传送横幅中。</span><span class="sxs-lookup"><span data-stu-id="c088e-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="c088e-107">例如，零售商可在主页中使用传送模块展示多个新产品或促销。</span><span class="sxs-lookup"><span data-stu-id="c088e-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="c088e-108">可以在传送模块中添加内容块模块。</span><span class="sxs-lookup"><span data-stu-id="c088e-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="c088e-109">然后，传送模块的属性定义如何显示这些模块。</span><span class="sxs-lookup"><span data-stu-id="c088e-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="c088e-110">电子商务中的传送模块示例</span><span class="sxs-lookup"><span data-stu-id="c088e-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="c088e-111">可在主页中使用内部有多个促销模块的传送。</span><span class="sxs-lookup"><span data-stu-id="c088e-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="c088e-112">可在产品详细信息页中使用内部有多个促销模块的传送。</span><span class="sxs-lookup"><span data-stu-id="c088e-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="c088e-113">可在任何市场营销页中使用传送来促销多个促销或产品。</span><span class="sxs-lookup"><span data-stu-id="c088e-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="c088e-114">传送模块属性</span><span class="sxs-lookup"><span data-stu-id="c088e-114">Carousel module properties</span></span>

| <span data-ttu-id="c088e-115">属性名称</span><span class="sxs-lookup"><span data-stu-id="c088e-115">Property name</span></span>             | <span data-ttu-id="c088e-116">值</span><span class="sxs-lookup"><span data-stu-id="c088e-116">Value</span></span>                 | <span data-ttu-id="c088e-117">说明</span><span class="sxs-lookup"><span data-stu-id="c088e-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="c088e-118">自动播放</span><span class="sxs-lookup"><span data-stu-id="c088e-118">Autoplay</span></span>                  | <span data-ttu-id="c088e-119">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="c088e-119">**True** or **False**</span></span> | <span data-ttu-id="c088e-120">如果此值设置为 **True**，将自动在传送内的项之间进行切换。</span><span class="sxs-lookup"><span data-stu-id="c088e-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="c088e-121">如果此值设置为 **False**，则除非客户使用键盘或鼠标从一个项移到下一个项，否则不进行切换。</span><span class="sxs-lookup"><span data-stu-id="c088e-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="c088e-122">幻灯片切换间隔</span><span class="sxs-lookup"><span data-stu-id="c088e-122">Slide transition interval</span></span> | <span data-ttu-id="c088e-123">以秒为单位的值</span><span class="sxs-lookup"><span data-stu-id="c088e-123">A value in seconds</span></span>    | <span data-ttu-id="c088e-124">项之间的切换间隔。</span><span class="sxs-lookup"><span data-stu-id="c088e-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="c088e-125">转换类型</span><span class="sxs-lookup"><span data-stu-id="c088e-125">Transition type</span></span>           | <span data-ttu-id="c088e-126">**幻灯片**或**淡化**</span><span class="sxs-lookup"><span data-stu-id="c088e-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="c088e-127">项目之间的过渡效果。</span><span class="sxs-lookup"><span data-stu-id="c088e-127">The transition effect between items.</span></span> |
| <span data-ttu-id="c088e-128">隐藏轮播翻转器</span><span class="sxs-lookup"><span data-stu-id="c088e-128">Hide carousel flipper</span></span>     | <span data-ttu-id="c088e-129">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="c088e-129">**True** or **False**</span></span> | <span data-ttu-id="c088e-130">如果该值设置为 **True**，轮播翻转器和顺序指示器将被隐藏。</span><span class="sxs-lookup"><span data-stu-id="c088e-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="c088e-131">允许轮播消除</span><span class="sxs-lookup"><span data-stu-id="c088e-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="c088e-132">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="c088e-132">**True** or **False**</span></span> | <span data-ttu-id="c088e-133">如果此值设置为 **True**，则用户可消除轮播。</span><span class="sxs-lookup"><span data-stu-id="c088e-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="c088e-134">向页面添加传送模块</span><span class="sxs-lookup"><span data-stu-id="c088e-134">Add a carousel module to a page</span></span>

<span data-ttu-id="c088e-135">若要向新页面添加传送模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c088e-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c088e-136">创建一个名称为**传送模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="c088e-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="c088e-137">在**正文**插槽中，添加一个**默认页面**模块。</span><span class="sxs-lookup"><span data-stu-id="c088e-137">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="c088e-138">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="c088e-138">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="c088e-139">使用您刚才创建的传送模板创建一个名称为**传送页**的页面。</span><span class="sxs-lookup"><span data-stu-id="c088e-139">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="c088e-140">在新页的**主**插槽中，添加一个容器模块。</span><span class="sxs-lookup"><span data-stu-id="c088e-140">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="c088e-141">在右侧窗格中，将**宽度**值设置为**填充屏幕**。</span><span class="sxs-lookup"><span data-stu-id="c088e-141">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="c088e-142">在**页面大纲**下面，将传送模块添加到容器模块中。</span><span class="sxs-lookup"><span data-stu-id="c088e-142">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="c088e-143">向该传送模块添加一个内容块模块。</span><span class="sxs-lookup"><span data-stu-id="c088e-143">Add a content block module to the carousel module.</span></span> <span data-ttu-id="c088e-144">通过提供**标题**、**链接**、**布局**和其他属性来设置内容块模块的属性。</span><span class="sxs-lookup"><span data-stu-id="c088e-144">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="c088e-145">添加并配置另一个内容块模块。</span><span class="sxs-lookup"><span data-stu-id="c088e-145">Add and configure another content block module.</span></span>
1. <span data-ttu-id="c088e-146">根据需要为传送模块设置其他属性。</span><span class="sxs-lookup"><span data-stu-id="c088e-146">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="c088e-147">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="c088e-147">Save and preview the page.</span></span> <span data-ttu-id="c088e-148">此页应该显示一个传送，其中有两个模块（即主图模块和特色模块）。</span><span class="sxs-lookup"><span data-stu-id="c088e-148">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="c088e-149">可以更改传送、主图和特色模块的其他属性以获得所需效果。</span><span class="sxs-lookup"><span data-stu-id="c088e-149">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="c088e-150">编辑完页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="c088e-150">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c088e-151">其他资源</span><span class="sxs-lookup"><span data-stu-id="c088e-151">Additional resources</span></span>

[<span data-ttu-id="c088e-152">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="c088e-152">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c088e-153">促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="c088e-153">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="c088e-154">文本块模块</span><span class="sxs-lookup"><span data-stu-id="c088e-154">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="c088e-155">内容块模块</span><span class="sxs-lookup"><span data-stu-id="c088e-155">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="c088e-156">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="c088e-156">Video player module</span></span>](add-video-player.md)
