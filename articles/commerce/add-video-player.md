---
title: 视频播放器模块
description: 此主题介绍视频播放器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025635"
---
# <a name="video-player-module"></a><span data-ttu-id="28d58-103">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="28d58-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="28d58-104">此主题介绍视频播放器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="28d58-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="28d58-105">概览</span><span class="sxs-lookup"><span data-stu-id="28d58-105">Overview</span></span>

<span data-ttu-id="28d58-106">视频播放器模块用于支持视频播放。</span><span class="sxs-lookup"><span data-stu-id="28d58-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="28d58-107">只要视频内容已上传到内容管理系统 (CMS) 并在其中可用，就可以将它添加到任何页面。</span><span class="sxs-lookup"><span data-stu-id="28d58-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="28d58-108">视频播放器模块支持 .mp4 媒体类型。</span><span class="sxs-lookup"><span data-stu-id="28d58-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="28d58-109">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="28d58-109">Video player module</span></span>

<span data-ttu-id="28d58-110">可在电子商务站点中使用视频播放器模块展示视频。</span><span class="sxs-lookup"><span data-stu-id="28d58-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="28d58-111">它支持所有播放功能，如播放、暂停、全屏模式、音频描述和隐藏式字幕。</span><span class="sxs-lookup"><span data-stu-id="28d58-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="28d58-112">视频播放器模块还支持自定义隐藏式字幕以满足 Microsoft 的辅助功能标准。</span><span class="sxs-lookup"><span data-stu-id="28d58-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="28d58-113">例如，可自定义字体大小和背景色。</span><span class="sxs-lookup"><span data-stu-id="28d58-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="28d58-114">视频播放器模块还支持辅助音轨。</span><span class="sxs-lookup"><span data-stu-id="28d58-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="28d58-115">将视频上载到 CMS 后，还可以上载辅助音轨。</span><span class="sxs-lookup"><span data-stu-id="28d58-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="28d58-116">然后，如果用户选择了视频播放器模块，它则可以播放辅助音轨。</span><span class="sxs-lookup"><span data-stu-id="28d58-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="28d58-117">电子商务中的视频播放器模块示例</span><span class="sxs-lookup"><span data-stu-id="28d58-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="28d58-118">产品详细信息页或市场营销页上的说明性视频</span><span class="sxs-lookup"><span data-stu-id="28d58-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="28d58-119">任何市场营销页上的促销视频或有关政策的视频</span><span class="sxs-lookup"><span data-stu-id="28d58-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="28d58-120">产品详细信息页或市场营销页上重点介绍产品特色的市场营销视频</span><span class="sxs-lookup"><span data-stu-id="28d58-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="28d58-121">视频播放器模块属性</span><span class="sxs-lookup"><span data-stu-id="28d58-121">Video player module properties</span></span>

| <span data-ttu-id="28d58-122">属性名称</span><span class="sxs-lookup"><span data-stu-id="28d58-122">Property name</span></span>         | <span data-ttu-id="28d58-123">值</span><span class="sxs-lookup"><span data-stu-id="28d58-123">Value</span></span>                               | <span data-ttu-id="28d58-124">说明</span><span class="sxs-lookup"><span data-stu-id="28d58-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="28d58-125">自动播放</span><span class="sxs-lookup"><span data-stu-id="28d58-125">Auto play</span></span>             | <span data-ttu-id="28d58-126">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="28d58-126">**True** or **False**</span></span>               | <span data-ttu-id="28d58-127">如果此值设置为 **True**，将自动播放视频。</span><span class="sxs-lookup"><span data-stu-id="28d58-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="28d58-128">静音</span><span class="sxs-lookup"><span data-stu-id="28d58-128">Mute</span></span>                  | <span data-ttu-id="28d58-129">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="28d58-129">**True** or **False**</span></span>               | <span data-ttu-id="28d58-130">如果此值设置为 **True**，将静音。</span><span class="sxs-lookup"><span data-stu-id="28d58-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="28d58-131">对于此播放器，默认值为 **False**。</span><span class="sxs-lookup"><span data-stu-id="28d58-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="28d58-132">在 Chrome 浏览器中，自动播放的视频默认静音，仅当用户手动播放视频时，才播放音频。</span><span class="sxs-lookup"><span data-stu-id="28d58-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="28d58-133">循环</span><span class="sxs-lookup"><span data-stu-id="28d58-133">Loop</span></span>                  | <span data-ttu-id="28d58-134">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="28d58-134">**True** or **False**</span></span>               | <span data-ttu-id="28d58-135">如果此值设置为 **True**，将循环重复播放视频。</span><span class="sxs-lookup"><span data-stu-id="28d58-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="28d58-136">媒体</span><span class="sxs-lookup"><span data-stu-id="28d58-136">Media</span></span>                 | <span data-ttu-id="28d58-137">视频文件路径和名称</span><span class="sxs-lookup"><span data-stu-id="28d58-137">Video file path and name</span></span> | <span data-ttu-id="28d58-138">视频播放器中播放的视频文件。</span><span class="sxs-lookup"><span data-stu-id="28d58-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="28d58-139">全屏播放</span><span class="sxs-lookup"><span data-stu-id="28d58-139">Play fullscreen</span></span>       | <span data-ttu-id="28d58-140">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="28d58-140">**True** or **False**</span></span>               | <span data-ttu-id="28d58-141">如果此值设置为 **True**，将以全屏模式播放视频。</span><span class="sxs-lookup"><span data-stu-id="28d58-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="28d58-142">播放暂停触发器</span><span class="sxs-lookup"><span data-stu-id="28d58-142">Play pause trigger</span></span>    | <span data-ttu-id="28d58-143">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="28d58-143">**True** or **False**</span></span>               | <span data-ttu-id="28d58-144">如果此值设置为 **True**，视频中将显示播放/暂停按钮。</span><span class="sxs-lookup"><span data-stu-id="28d58-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="28d58-145">视频播放器控件</span><span class="sxs-lookup"><span data-stu-id="28d58-145">Video player controls</span></span> | <span data-ttu-id="28d58-146">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="28d58-146">**True** or **False**</span></span>               | <span data-ttu-id="28d58-147">如果此值设置为 **True**，将显示所有视频播放器控件。</span><span class="sxs-lookup"><span data-stu-id="28d58-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="28d58-148">这些控件包括播放和暂停按钮、进度指示器和隐藏式字幕选项。</span><span class="sxs-lookup"><span data-stu-id="28d58-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="28d58-149">隐藏海报图像</span><span class="sxs-lookup"><span data-stu-id="28d58-149">Hide poster image</span></span>     | <span data-ttu-id="28d58-150">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="28d58-150">**True** or **False**</span></span>               | <span data-ttu-id="28d58-151">视频可具有海报框架。</span><span class="sxs-lookup"><span data-stu-id="28d58-151">A video can have a poster frame.</span></span> <span data-ttu-id="28d58-152">如果此属性的值设置为 **True**，将隐藏海报框架。</span><span class="sxs-lookup"><span data-stu-id="28d58-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="28d58-153">蒙板级别</span><span class="sxs-lookup"><span data-stu-id="28d58-153">Mask level</span></span>            | <span data-ttu-id="28d58-154">从 **0** 到 **100** 的数字</span><span class="sxs-lookup"><span data-stu-id="28d58-154">A number from **0** through **100**</span></span> | <span data-ttu-id="28d58-155">为风格而向视频应用的蒙板。</span><span class="sxs-lookup"><span data-stu-id="28d58-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="28d58-156">向页面添加视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="28d58-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="28d58-157">在创建视频播放器模块之前，必须首先将视频上传到媒体库。</span><span class="sxs-lookup"><span data-stu-id="28d58-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="28d58-158">若要向新页面添加视频播放器模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="28d58-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="28d58-159">创建一个名称为**视频播放器模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="28d58-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="28d58-160">在默认页的**主**插槽中，添加一个容器模块。</span><span class="sxs-lookup"><span data-stu-id="28d58-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="28d58-161">在容器模块中，添加视频播放器模块和氛围视频播放器模块。</span><span class="sxs-lookup"><span data-stu-id="28d58-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="28d58-162">编辑完模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="28d58-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="28d58-163">使用您创建的视频播放器模板创建一个名称为**视频播放器页**的页面。</span><span class="sxs-lookup"><span data-stu-id="28d58-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="28d58-164">在新页的**主**插槽中，添加一个视频播放器模块。</span><span class="sxs-lookup"><span data-stu-id="28d58-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="28d58-165">在视频播放器模块的属性窗格中，选择**添加视频**。</span><span class="sxs-lookup"><span data-stu-id="28d58-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="28d58-166">在**媒体选择器**对话框中，选择一个视频，然后选择**上载新媒体项目**。</span><span class="sxs-lookup"><span data-stu-id="28d58-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="28d58-167">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="28d58-167">Save and preview the page.</span></span> <span data-ttu-id="28d58-168">应该可以在页面中看到此视频模块。</span><span class="sxs-lookup"><span data-stu-id="28d58-168">You should see the video module on the page.</span></span> <span data-ttu-id="28d58-169">可以更改更多属性以自定义模块的行为。</span><span class="sxs-lookup"><span data-stu-id="28d58-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="28d58-170">编辑完页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="28d58-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28d58-171">其他资源</span><span class="sxs-lookup"><span data-stu-id="28d58-171">Additional resources</span></span>

[<span data-ttu-id="28d58-172">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="28d58-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="28d58-173">促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="28d58-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="28d58-174">传送模块</span><span class="sxs-lookup"><span data-stu-id="28d58-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="28d58-175">文本块模块</span><span class="sxs-lookup"><span data-stu-id="28d58-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="28d58-176">内容块模块</span><span class="sxs-lookup"><span data-stu-id="28d58-176">Content block module</span></span>](add-hero-module.md)
