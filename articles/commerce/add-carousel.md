---
title: 传送模块
description: 此主题介绍传送模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269720"
---
# <a name="carousel-module"></a><span data-ttu-id="64267-103">传送模块</span><span class="sxs-lookup"><span data-stu-id="64267-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="64267-104">此主题介绍传送模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="64267-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="64267-105">概览</span><span class="sxs-lookup"><span data-stu-id="64267-105">Overview</span></span>

<span data-ttu-id="64267-106">传送模块用于将多个促销项（包括大量图像）放到客户可浏览的旋转式传送横幅中。</span><span class="sxs-lookup"><span data-stu-id="64267-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="64267-107">例如，零售商可在主页中使用传送模块展示多个新产品或促销。</span><span class="sxs-lookup"><span data-stu-id="64267-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="64267-108">可以在传送模块中添加内容块模块。</span><span class="sxs-lookup"><span data-stu-id="64267-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="64267-109">然后，传送模块的属性定义如何显示这些模块。</span><span class="sxs-lookup"><span data-stu-id="64267-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="64267-110">电子商务中的传送模块示例</span><span class="sxs-lookup"><span data-stu-id="64267-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="64267-111">可在主页中使用内部有多个促销模块的传送。</span><span class="sxs-lookup"><span data-stu-id="64267-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="64267-112">可在产品详细信息页中使用内部有多个促销模块的传送。</span><span class="sxs-lookup"><span data-stu-id="64267-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="64267-113">可在任何市场营销页中使用传送来促销多个促销或产品。</span><span class="sxs-lookup"><span data-stu-id="64267-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="64267-114">传送模块属性</span><span class="sxs-lookup"><span data-stu-id="64267-114">Carousel module properties</span></span>

| <span data-ttu-id="64267-115">属性名称</span><span class="sxs-lookup"><span data-stu-id="64267-115">Property name</span></span>             | <span data-ttu-id="64267-116">值</span><span class="sxs-lookup"><span data-stu-id="64267-116">Value</span></span>                 | <span data-ttu-id="64267-117">说明</span><span class="sxs-lookup"><span data-stu-id="64267-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="64267-118">自动播放</span><span class="sxs-lookup"><span data-stu-id="64267-118">Autoplay</span></span>                  | <span data-ttu-id="64267-119">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="64267-119">**True** or **False**</span></span> | <span data-ttu-id="64267-120">如果此值设置为 **True**，将自动在传送内的项之间进行切换。</span><span class="sxs-lookup"><span data-stu-id="64267-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="64267-121">如果此值设置为 **False**，则除非客户使用键盘或鼠标从一个项移到下一个项，否则不进行切换。</span><span class="sxs-lookup"><span data-stu-id="64267-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="64267-122">幻灯片切换间隔</span><span class="sxs-lookup"><span data-stu-id="64267-122">Slide transition interval</span></span> | <span data-ttu-id="64267-123">以秒为单位的值</span><span class="sxs-lookup"><span data-stu-id="64267-123">A value in seconds</span></span>    | <span data-ttu-id="64267-124">项之间的切换间隔。</span><span class="sxs-lookup"><span data-stu-id="64267-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="64267-125">转换类型</span><span class="sxs-lookup"><span data-stu-id="64267-125">Transition type</span></span>           | <span data-ttu-id="64267-126">**幻灯片**或**淡化**</span><span class="sxs-lookup"><span data-stu-id="64267-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="64267-127">项目之间的过渡效果。</span><span class="sxs-lookup"><span data-stu-id="64267-127">The transition effect between items.</span></span> |
| <span data-ttu-id="64267-128">隐藏轮播翻转器</span><span class="sxs-lookup"><span data-stu-id="64267-128">Hide carousel flipper</span></span>     | <span data-ttu-id="64267-129">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="64267-129">**True** or **False**</span></span> | <span data-ttu-id="64267-130">如果该值设置为 **True**，轮播翻转器和顺序指示器将被隐藏。</span><span class="sxs-lookup"><span data-stu-id="64267-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="64267-131">允许轮播消除</span><span class="sxs-lookup"><span data-stu-id="64267-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="64267-132">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="64267-132">**True** or **False**</span></span> | <span data-ttu-id="64267-133">如果此值设置为 **True**，则用户可消除轮播。</span><span class="sxs-lookup"><span data-stu-id="64267-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="64267-134">向页面添加传送模块</span><span class="sxs-lookup"><span data-stu-id="64267-134">Add a carousel module to a page</span></span>

<span data-ttu-id="64267-135">若要向新页面添加传送模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="64267-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="64267-136">选择**新建**以创建页面模板。</span><span class="sxs-lookup"><span data-stu-id="64267-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="64267-137">在**新建模板**对话框的**模板名称**下，输入**传送模板**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="64267-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="64267-138">在**正文**插槽中，添加一个**默认页面**模块。</span><span class="sxs-lookup"><span data-stu-id="64267-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="64267-139">选择**完成编辑**签入模板，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="64267-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="64267-140">使用您刚才创建的传送模板创建一个名称为**传送页**的页面。</span><span class="sxs-lookup"><span data-stu-id="64267-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="64267-141">在新页的**主**插槽中，添加一个容器模块。</span><span class="sxs-lookup"><span data-stu-id="64267-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="64267-142">在右侧窗格中，将**宽度**值设置为**填充屏幕**。</span><span class="sxs-lookup"><span data-stu-id="64267-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="64267-143">在**页面大纲**下面，将传送模块添加到容器模块中。</span><span class="sxs-lookup"><span data-stu-id="64267-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="64267-144">向该传送模块添加一个内容块模块。</span><span class="sxs-lookup"><span data-stu-id="64267-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="64267-145">通过提供**标题**、**链接**、**布局**和其他属性来设置内容块模块的属性。</span><span class="sxs-lookup"><span data-stu-id="64267-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="64267-146">添加并配置另一个内容块模块。</span><span class="sxs-lookup"><span data-stu-id="64267-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="64267-147">根据需要为传送模块设置其他属性。</span><span class="sxs-lookup"><span data-stu-id="64267-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="64267-148">选择**保存**，然后选择**预览**以预览页面。</span><span class="sxs-lookup"><span data-stu-id="64267-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="64267-149">此页应该显示一个传送，其中有两个模块（即主图模块和特色模块）。</span><span class="sxs-lookup"><span data-stu-id="64267-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="64267-150">可以更改传送、主图和特色模块的其他属性以获得所需效果。</span><span class="sxs-lookup"><span data-stu-id="64267-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="64267-151">选择**完成编辑**签入页面，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="64267-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64267-152">其他资源</span><span class="sxs-lookup"><span data-stu-id="64267-152">Additional resources</span></span>

[<span data-ttu-id="64267-153">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="64267-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="64267-154">促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="64267-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="64267-155">文本块模块</span><span class="sxs-lookup"><span data-stu-id="64267-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="64267-156">内容块模块</span><span class="sxs-lookup"><span data-stu-id="64267-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="64267-157">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="64267-157">Video player module</span></span>](add-video-player.md)
