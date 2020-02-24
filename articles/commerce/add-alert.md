---
title: 促销横幅模块
description: 此主题介绍促销横幅模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025612"
---
# <a name="promo-banner-module"></a><span data-ttu-id="c9841-103">促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="c9841-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c9841-104">此主题介绍促销横幅模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="c9841-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c9841-105">概览</span><span class="sxs-lookup"><span data-stu-id="c9841-105">Overview</span></span>

<span data-ttu-id="c9841-106">促销横幅模块用于在页面中显示内联参考消息。</span><span class="sxs-lookup"><span data-stu-id="c9841-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="c9841-107">可用于显示电子商务站点所有页面中显示的站点范围促销。</span><span class="sxs-lookup"><span data-stu-id="c9841-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="c9841-108">促销横幅模块支持文本消息和链接。</span><span class="sxs-lookup"><span data-stu-id="c9841-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="c9841-109">如果将多个消息添加到促销横幅模块，它将变成旋转的轮播横幅，使客户可以循环浏览所有消息。</span><span class="sxs-lookup"><span data-stu-id="c9841-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="c9841-110">促销横幅模块由内容管理系统 (CMS) 的数据驱动，可放到任何页面中。</span><span class="sxs-lookup"><span data-stu-id="c9841-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="c9841-111">电子商务中促销横幅的用法示例</span><span class="sxs-lookup"><span data-stu-id="c9841-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="c9841-112">可以在网站标题中使用促销横幅，以显示网站范围内的促销或消息，如以下示例所示。</span><span class="sxs-lookup"><span data-stu-id="c9841-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="c9841-113">“年度促销 10 天后结束”</span><span class="sxs-lookup"><span data-stu-id="c9841-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="c9841-114">“返校季大促销。</span><span class="sxs-lookup"><span data-stu-id="c9841-114">"Save big with back to school sale.</span></span> <span data-ttu-id="c9841-115">快来买啦。”</span><span class="sxs-lookup"><span data-stu-id="c9841-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="c9841-116">促销横幅模块属性</span><span class="sxs-lookup"><span data-stu-id="c9841-116">Promo banner module properties</span></span>

| <span data-ttu-id="c9841-117">属性名称</span><span class="sxs-lookup"><span data-stu-id="c9841-117">Property name</span></span>             | <span data-ttu-id="c9841-118">Value</span><span class="sxs-lookup"><span data-stu-id="c9841-118">Value</span></span>                              | <span data-ttu-id="c9841-119">说明</span><span class="sxs-lookup"><span data-stu-id="c9841-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="c9841-120">横幅消息</span><span class="sxs-lookup"><span data-stu-id="c9841-120">Banner messages</span></span>           | <span data-ttu-id="c9841-121">文本和链接</span><span class="sxs-lookup"><span data-stu-id="c9841-121">Text and links</span></span>                     | <span data-ttu-id="c9841-122">文本和链接的数组。</span><span class="sxs-lookup"><span data-stu-id="c9841-122">An array of text and links.</span></span> |
| <span data-ttu-id="c9841-123">自动播放</span><span class="sxs-lookup"><span data-stu-id="c9841-123">Autoplay</span></span>                  | <span data-ttu-id="c9841-124">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="c9841-124">**True** or **False**</span></span>              | <span data-ttu-id="c9841-125">一个值，指示如果配置了多个消息，则是否自动循环显示消息。</span><span class="sxs-lookup"><span data-stu-id="c9841-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="c9841-126">幻灯片切换间隔</span><span class="sxs-lookup"><span data-stu-id="c9841-126">Slide transition interval</span></span> | <span data-ttu-id="c9841-127">毫秒数</span><span class="sxs-lookup"><span data-stu-id="c9841-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="c9841-128">用于循环浏览消息的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="c9841-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="c9841-129">允许消除</span><span class="sxs-lookup"><span data-stu-id="c9841-129">Allow dismiss</span></span>             | <span data-ttu-id="c9841-130">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="c9841-130">**True** or **False**</span></span>              | <span data-ttu-id="c9841-131">如果此值设置为 **True**，则客户可忽略预警。</span><span class="sxs-lookup"><span data-stu-id="c9841-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="c9841-132">显示轮播翻转器</span><span class="sxs-lookup"><span data-stu-id="c9841-132">Show carousel flipper</span></span>     | <span data-ttu-id="c9841-133">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="c9841-133">**True** or **False**</span></span>              | <span data-ttu-id="c9841-134">一个值，该值指示是否应显示轮播翻转器，以便客户可以手动循环浏览多个横幅项目。</span><span class="sxs-lookup"><span data-stu-id="c9841-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="c9841-135">文本对齐</span><span class="sxs-lookup"><span data-stu-id="c9841-135">Text alignment</span></span>            | <span data-ttu-id="c9841-136">**向右对齐**、**向左对齐**或**居中对齐**</span><span class="sxs-lookup"><span data-stu-id="c9841-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="c9841-137">促销横幅模块中的文本对齐。</span><span class="sxs-lookup"><span data-stu-id="c9841-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="c9841-138">链接</span><span class="sxs-lookup"><span data-stu-id="c9841-138">Link</span></span>                      | <span data-ttu-id="c9841-139">URL</span><span class="sxs-lookup"><span data-stu-id="c9841-139">A URL</span></span>                              | <span data-ttu-id="c9841-140">可选链接的 URL。</span><span class="sxs-lookup"><span data-stu-id="c9841-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="c9841-141">向页面添加促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="c9841-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="c9841-142">若要向页面添加促销横幅模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c9841-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c9841-143">创建一个名称为**促销横幅模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="c9841-143">Create a page template that is named **Promo banner template**.</span></span>
1. <span data-ttu-id="c9841-144">在**页面大纲**下面，将**默认页面**模块添加到**正文**插槽中。</span><span class="sxs-lookup"><span data-stu-id="c9841-144">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="c9841-145">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="c9841-145">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="c9841-146">使用您刚才创建的模板创建一个名称为**促销横幅页**的页面。</span><span class="sxs-lookup"><span data-stu-id="c9841-146">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="c9841-147">在新页的**主**插槽中，添加一个容器模块。</span><span class="sxs-lookup"><span data-stu-id="c9841-147">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="c9841-148">在右侧窗格中，将**宽度**值设置为**填充容器**。</span><span class="sxs-lookup"><span data-stu-id="c9841-148">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="c9841-149">在**页面大纲**下面，将促销横幅模块添加到容器模块中。</span><span class="sxs-lookup"><span data-stu-id="c9841-149">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="c9841-150">在横幅模块的设置中，添加一个或多个横幅消息。</span><span class="sxs-lookup"><span data-stu-id="c9841-150">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="c9841-151">每条消息都可以具有带有链接的文本。</span><span class="sxs-lookup"><span data-stu-id="c9841-151">Each message can have text together with a link.</span></span> <span data-ttu-id="c9841-152">可以编辑其他属性以进一步自定义模块。</span><span class="sxs-lookup"><span data-stu-id="c9841-152">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="c9841-153">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="c9841-153">Save and preview the page.</span></span> <span data-ttu-id="c9841-154">在页面顶部，应该会看到显示您添加的文本的预警。</span><span class="sxs-lookup"><span data-stu-id="c9841-154">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="c9841-155">编辑完页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="c9841-155">Finish editing the page, and publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="c9841-156">通常在页面标题槽或子标题槽中使用促销横幅。</span><span class="sxs-lookup"><span data-stu-id="c9841-156">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="c9841-157">其他资源</span><span class="sxs-lookup"><span data-stu-id="c9841-157">Additional resources</span></span>

[<span data-ttu-id="c9841-158">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="c9841-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c9841-159">传送模块</span><span class="sxs-lookup"><span data-stu-id="c9841-159">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="c9841-160">文本块模块</span><span class="sxs-lookup"><span data-stu-id="c9841-160">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="c9841-161">内容块模块</span><span class="sxs-lookup"><span data-stu-id="c9841-161">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="c9841-162">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="c9841-162">Video player module</span></span>](add-video-player.md)
