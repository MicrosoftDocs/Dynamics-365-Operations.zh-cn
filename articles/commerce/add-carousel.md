---
title: 传送模块
description: 此主题介绍传送模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
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
ms.openlocfilehash: 0b4ce8fdb7b598e55db59ddf5a99a0ba46eb6f91
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985996"
---
# <a name="carousel-module"></a><span data-ttu-id="36570-103">传送模块</span><span class="sxs-lookup"><span data-stu-id="36570-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="36570-104">此主题介绍传送模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="36570-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="36570-105">概览</span><span class="sxs-lookup"><span data-stu-id="36570-105">Overview</span></span>

<span data-ttu-id="36570-106">传送模块用于将多个促销项（包括大量图像）放到客户可浏览的旋转式传送横幅中。</span><span class="sxs-lookup"><span data-stu-id="36570-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="36570-107">例如，零售商可在主页中使用传送模块展示多个新产品或促销。</span><span class="sxs-lookup"><span data-stu-id="36570-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="36570-108">可以在传送模块中添加内容块模块。</span><span class="sxs-lookup"><span data-stu-id="36570-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="36570-109">然后，传送模块的属性定义如何显示这些模块。</span><span class="sxs-lookup"><span data-stu-id="36570-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="36570-110">电子商务中的传送模块示例</span><span class="sxs-lookup"><span data-stu-id="36570-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="36570-111">可在主页中使用内部有多个促销模块的传送。</span><span class="sxs-lookup"><span data-stu-id="36570-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="36570-112">可在产品详细信息页中使用内部有多个促销模块的传送。</span><span class="sxs-lookup"><span data-stu-id="36570-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="36570-113">可在任何市场营销页中使用传送来促销多个促销或产品。</span><span class="sxs-lookup"><span data-stu-id="36570-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="36570-114">下图显示了主页上使用的传送模块的示例。</span><span class="sxs-lookup"><span data-stu-id="36570-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="36570-115">此传送模块包含多个内容块项。</span><span class="sxs-lookup"><span data-stu-id="36570-115">This carousel module contains multiple content block items.</span></span>

![传送模块的示例](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="36570-117">传送模块属性</span><span class="sxs-lookup"><span data-stu-id="36570-117">Carousel module properties</span></span>

| <span data-ttu-id="36570-118">属性名称</span><span class="sxs-lookup"><span data-stu-id="36570-118">Property name</span></span>             | <span data-ttu-id="36570-119">值</span><span class="sxs-lookup"><span data-stu-id="36570-119">Value</span></span>                 | <span data-ttu-id="36570-120">说明</span><span class="sxs-lookup"><span data-stu-id="36570-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="36570-121">自动播放</span><span class="sxs-lookup"><span data-stu-id="36570-121">Autoplay</span></span>                  | <span data-ttu-id="36570-122">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="36570-122">**True** or **False**</span></span> | <span data-ttu-id="36570-123">如果此值设置为 **True**，将自动在传送内的项之间进行切换。</span><span class="sxs-lookup"><span data-stu-id="36570-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="36570-124">如果此值设置为 **False**，则除非客户使用键盘或鼠标从一个项移到下一个项，否则不进行切换。</span><span class="sxs-lookup"><span data-stu-id="36570-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="36570-125">幻灯片切换间隔</span><span class="sxs-lookup"><span data-stu-id="36570-125">Slide transition interval</span></span> | <span data-ttu-id="36570-126">以秒为单位的值</span><span class="sxs-lookup"><span data-stu-id="36570-126">A value in seconds</span></span>    | <span data-ttu-id="36570-127">项之间的切换间隔。</span><span class="sxs-lookup"><span data-stu-id="36570-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="36570-128">转换类型</span><span class="sxs-lookup"><span data-stu-id="36570-128">Transition type</span></span>           | <span data-ttu-id="36570-129">**幻灯片** 或 **淡化**</span><span class="sxs-lookup"><span data-stu-id="36570-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="36570-130">项目之间的过渡效果。</span><span class="sxs-lookup"><span data-stu-id="36570-130">The transition effect between items.</span></span> |
| <span data-ttu-id="36570-131">隐藏轮播翻转器</span><span class="sxs-lookup"><span data-stu-id="36570-131">Hide carousel flipper</span></span>     | <span data-ttu-id="36570-132">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="36570-132">**True** or **False**</span></span> | <span data-ttu-id="36570-133">如果该值设置为 **True**，轮播翻转器和顺序指示器将被隐藏。</span><span class="sxs-lookup"><span data-stu-id="36570-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="36570-134">允许轮播消除</span><span class="sxs-lookup"><span data-stu-id="36570-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="36570-135">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="36570-135">**True** or **False**</span></span> | <span data-ttu-id="36570-136">如果此值设置为 **True**，则用户可消除轮播。</span><span class="sxs-lookup"><span data-stu-id="36570-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="36570-137">向页面添加传送模块</span><span class="sxs-lookup"><span data-stu-id="36570-137">Add a carousel module to a page</span></span>

<span data-ttu-id="36570-138">若要向新页面添加传送模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="36570-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="36570-139">转到 **模板**，选择 **新建** 创建新模板。</span><span class="sxs-lookup"><span data-stu-id="36570-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="36570-140">在 **新建模板** 对话框的 **模板名称** 下，输入 **传送模板**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="36570-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="36570-141">在 **正文** 插槽中，添加一个 **默认页面** 模块。</span><span class="sxs-lookup"><span data-stu-id="36570-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="36570-142">选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="36570-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="36570-143">使用您刚才创建的传送模板创建一个名称为 **传送页** 的页面。</span><span class="sxs-lookup"><span data-stu-id="36570-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="36570-144">在新页的 **主** 插槽中，添加一个容器模块。</span><span class="sxs-lookup"><span data-stu-id="36570-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="36570-145">在右侧窗格中，将 **宽度** 值设置为 **填充屏幕**。</span><span class="sxs-lookup"><span data-stu-id="36570-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="36570-146">在 **页面大纲** 下面，将传送模块添加到容器模块中。</span><span class="sxs-lookup"><span data-stu-id="36570-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="36570-147">向该传送模块添加一个内容块模块。</span><span class="sxs-lookup"><span data-stu-id="36570-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="36570-148">通过提供 **标题**、**链接**、**布局** 和其他属性来设置内容块模块的属性。</span><span class="sxs-lookup"><span data-stu-id="36570-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="36570-149">添加并配置另一个内容块模块。</span><span class="sxs-lookup"><span data-stu-id="36570-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="36570-150">根据需要为传送模块设置其他属性。</span><span class="sxs-lookup"><span data-stu-id="36570-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="36570-151">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="36570-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="36570-152">此页应该显示一个传送，其中有两个模块（即主图模块和特色模块）。</span><span class="sxs-lookup"><span data-stu-id="36570-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="36570-153">可以更改传送、主图和特色模块的其他属性以获得所需效果。</span><span class="sxs-lookup"><span data-stu-id="36570-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="36570-154">选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="36570-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36570-155">其他资源</span><span class="sxs-lookup"><span data-stu-id="36570-155">Additional resources</span></span>

[<span data-ttu-id="36570-156">模块库概述</span><span class="sxs-lookup"><span data-stu-id="36570-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="36570-157">促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="36570-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="36570-158">文本块模块</span><span class="sxs-lookup"><span data-stu-id="36570-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="36570-159">内容块模块</span><span class="sxs-lookup"><span data-stu-id="36570-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="36570-160">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="36570-160">Video player module</span></span>](add-video-player.md)
