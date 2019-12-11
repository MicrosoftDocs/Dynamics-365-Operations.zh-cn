---
title: 视频播放器模块
description: 此主题介绍视频播放器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 32504351f712c83ba8f593c17d2e51c532374311
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785321"
---
# <a name="video-player-module"></a><span data-ttu-id="e66ae-103">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="e66ae-103">Video player module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e66ae-104">此主题介绍视频播放器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="e66ae-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e66ae-105">概览</span><span class="sxs-lookup"><span data-stu-id="e66ae-105">Overview</span></span>

<span data-ttu-id="e66ae-106">视频播放器模块用于支持视频播放。</span><span class="sxs-lookup"><span data-stu-id="e66ae-106">Video player modules are used to support video playback.</span></span> <span data-ttu-id="e66ae-107">商店入门套件提供了两个视频播放器模块：氛围视频播放器模块和视频播放器模块。</span><span class="sxs-lookup"><span data-stu-id="e66ae-107">Two video player modules are provided in the store starter kit: the ambient video player module and the video player module.</span></span> <span data-ttu-id="e66ae-108">这两个播放器都支持 .mp4 媒体类型。</span><span class="sxs-lookup"><span data-stu-id="e66ae-108">Both players support the .mp4 media type.</span></span>

## <a name="ambient-video-player-module"></a><span data-ttu-id="e66ae-109">氛围视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="e66ae-109">Ambient video player module</span></span>

<span data-ttu-id="e66ae-110">氛围视频播放器模块支持信息性短视频。</span><span class="sxs-lookup"><span data-stu-id="e66ae-110">The ambient video player module supports short informational videos.</span></span> <span data-ttu-id="e66ae-111">其应该用于不超过五秒钟的视频。</span><span class="sxs-lookup"><span data-stu-id="e66ae-111">It should be used for videos that are less than five seconds long.</span></span> <span data-ttu-id="e66ae-112">这种播放器支持有限视频播放功能，如播放和暂停。</span><span class="sxs-lookup"><span data-stu-id="e66ae-112">This player supports limited video playback capabilities, such as play and pause.</span></span>

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a><span data-ttu-id="e66ae-113">电子商务中的氛围视频播放器模块示例</span><span class="sxs-lookup"><span data-stu-id="e66ae-113">Examples of ambient video player modules in e-Commerce</span></span>

- <span data-ttu-id="e66ae-114">主页中重点介绍新产品的信息性短视频</span><span class="sxs-lookup"><span data-stu-id="e66ae-114">Short informational videos that highlight new products on the home page</span></span>
- <span data-ttu-id="e66ae-115">产品详细信息页中重点介绍产品特色的信息性短视频</span><span class="sxs-lookup"><span data-stu-id="e66ae-115">Short informational videos that highlight product features on a product details page</span></span>

### <a name="ambient-video-player-module-properties"></a><span data-ttu-id="e66ae-116">氛围视频播放器模块属性</span><span class="sxs-lookup"><span data-stu-id="e66ae-116">Ambient video player module properties</span></span>

| <span data-ttu-id="e66ae-117">属性名称</span><span class="sxs-lookup"><span data-stu-id="e66ae-117">Property name</span></span>     | <span data-ttu-id="e66ae-118">值</span><span class="sxs-lookup"><span data-stu-id="e66ae-118">Value</span></span>                 | <span data-ttu-id="e66ae-119">说明</span><span class="sxs-lookup"><span data-stu-id="e66ae-119">Description</span></span> |
|-------------------|-----------------------|-------------|
| <span data-ttu-id="e66ae-120">自动播放</span><span class="sxs-lookup"><span data-stu-id="e66ae-120">Autoplay</span></span>          | <span data-ttu-id="e66ae-121">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e66ae-121">**True** or **False**</span></span> | <span data-ttu-id="e66ae-122">如果此值设置为 **True**，将自动播放视频。</span><span class="sxs-lookup"><span data-stu-id="e66ae-122">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="e66ae-123">静音</span><span class="sxs-lookup"><span data-stu-id="e66ae-123">Mute</span></span>              | <span data-ttu-id="e66ae-124">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e66ae-124">**True** or **False**</span></span> | <span data-ttu-id="e66ae-125">如果此值设置为 **True**，将静音。</span><span class="sxs-lookup"><span data-stu-id="e66ae-125">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="e66ae-126">对于此播放器，默认值为 **True**。</span><span class="sxs-lookup"><span data-stu-id="e66ae-126">For this player, the default value is **True**.</span></span> <span data-ttu-id="e66ae-127">在 Google Chrome 浏览器中，自动播放的视频默认静音，仅当用户手动播放视频时，才播放音频。</span><span class="sxs-lookup"><span data-stu-id="e66ae-127">In the Google Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="e66ae-128">循环</span><span class="sxs-lookup"><span data-stu-id="e66ae-128">Loop</span></span>              | <span data-ttu-id="e66ae-129">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e66ae-129">**True** or **False**</span></span> | <span data-ttu-id="e66ae-130">如果此值设置为 **True**，将循环重复播放视频。</span><span class="sxs-lookup"><span data-stu-id="e66ae-130">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="e66ae-131">媒体</span><span class="sxs-lookup"><span data-stu-id="e66ae-131">Media</span></span>             |  <span data-ttu-id="e66ae-132">视频文件路径和名称</span><span class="sxs-lookup"><span data-stu-id="e66ae-132">Video file path and name</span></span> | <span data-ttu-id="e66ae-133">视频播放器播放的视频文件。</span><span class="sxs-lookup"><span data-stu-id="e66ae-133">The video file that is played by the video player.</span></span> |
| <span data-ttu-id="e66ae-134">播放控制</span><span class="sxs-lookup"><span data-stu-id="e66ae-134">Playback controls</span></span> | <span data-ttu-id="e66ae-135">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e66ae-135">**True** or **False**</span></span> | <span data-ttu-id="e66ae-136">如果此值设置为 **True**，视频中将显示播放/暂停按钮。</span><span class="sxs-lookup"><span data-stu-id="e66ae-136">When the value is set to **True**, a play/pause button is shown on the video.</span></span> <span data-ttu-id="e66ae-137">如果此值设置为 **False**，将不显示播放/暂停按钮，当用户仍然可以使用键盘暂停和恢复播放视频。</span><span class="sxs-lookup"><span data-stu-id="e66ae-137">If the value is set to **False**, the play/pause button isn't shown, but users can still pause and resume the video by using the keyboard.</span></span> |

## <a name="video-player-module"></a><span data-ttu-id="e66ae-138">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="e66ae-138">Video player module</span></span>

<span data-ttu-id="e66ae-139">可在电子商务站点中使用视频播放器模块展示视频。</span><span class="sxs-lookup"><span data-stu-id="e66ae-139">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="e66ae-140">它支持所有播放功能，如播放、暂停、全屏模式和隐藏式字幕。</span><span class="sxs-lookup"><span data-stu-id="e66ae-140">It supports all playback capabilities, such as play, pause, full-size mode, and closed captions.</span></span> <span data-ttu-id="e66ae-141">视频播放器模块还支持自定义隐藏式字幕以满足 Microsoft 的辅助功能标准。</span><span class="sxs-lookup"><span data-stu-id="e66ae-141">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="e66ae-142">例如，可自定义字体大小和背景色。</span><span class="sxs-lookup"><span data-stu-id="e66ae-142">For example, you can customize the font size and background color.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="e66ae-143">电子商务中的视频播放器模块示例</span><span class="sxs-lookup"><span data-stu-id="e66ae-143">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="e66ae-144">产品详细信息页或市场营销页上的说明性视频</span><span class="sxs-lookup"><span data-stu-id="e66ae-144">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="e66ae-145">任何市场营销页上的促销视频或有关政策的视频</span><span class="sxs-lookup"><span data-stu-id="e66ae-145">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="e66ae-146">产品详细信息页或市场营销页上重点介绍产品特色的市场营销视频</span><span class="sxs-lookup"><span data-stu-id="e66ae-146">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="e66ae-147">视频播放器模块属性</span><span class="sxs-lookup"><span data-stu-id="e66ae-147">Video player module properties</span></span>

| <span data-ttu-id="e66ae-148">属性名称</span><span class="sxs-lookup"><span data-stu-id="e66ae-148">Property name</span></span>         | <span data-ttu-id="e66ae-149">值</span><span class="sxs-lookup"><span data-stu-id="e66ae-149">Value</span></span>                               | <span data-ttu-id="e66ae-150">说明</span><span class="sxs-lookup"><span data-stu-id="e66ae-150">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="e66ae-151">自动播放</span><span class="sxs-lookup"><span data-stu-id="e66ae-151">Auto play</span></span>             | <span data-ttu-id="e66ae-152">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e66ae-152">**True** or **False**</span></span>               | <span data-ttu-id="e66ae-153">如果此值设置为 **True**，将自动播放视频。</span><span class="sxs-lookup"><span data-stu-id="e66ae-153">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="e66ae-154">静音</span><span class="sxs-lookup"><span data-stu-id="e66ae-154">Mute</span></span>                  | <span data-ttu-id="e66ae-155">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e66ae-155">**True** or **False**</span></span>               | <span data-ttu-id="e66ae-156">如果此值设置为 **True**，将静音。</span><span class="sxs-lookup"><span data-stu-id="e66ae-156">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="e66ae-157">对于此播放器，默认值为 **False**。</span><span class="sxs-lookup"><span data-stu-id="e66ae-157">For this player, the default value is **False**.</span></span> <span data-ttu-id="e66ae-158">在 Chrome 浏览器中，自动播放的视频默认静音，仅当用户手动播放视频时，才播放音频。</span><span class="sxs-lookup"><span data-stu-id="e66ae-158">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="e66ae-159">循环</span><span class="sxs-lookup"><span data-stu-id="e66ae-159">Loop</span></span>                  | <span data-ttu-id="e66ae-160">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e66ae-160">**True** or **False**</span></span>               | <span data-ttu-id="e66ae-161">如果此值设置为 **True**，将循环重复播放视频。</span><span class="sxs-lookup"><span data-stu-id="e66ae-161">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="e66ae-162">媒体</span><span class="sxs-lookup"><span data-stu-id="e66ae-162">Media</span></span>                 | <span data-ttu-id="e66ae-163">视频文件路径和名称</span><span class="sxs-lookup"><span data-stu-id="e66ae-163">Video file path and name</span></span> | <span data-ttu-id="e66ae-164">视频播放器中播放的视频文件。</span><span class="sxs-lookup"><span data-stu-id="e66ae-164">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="e66ae-165">播放控制</span><span class="sxs-lookup"><span data-stu-id="e66ae-165">Playback controls</span></span>     | <span data-ttu-id="e66ae-166">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e66ae-166">**True** or **False**</span></span>               | <span data-ttu-id="e66ae-167">如果此值设置为 **True**，视频中将显示播放/暂停按钮。</span><span class="sxs-lookup"><span data-stu-id="e66ae-167">When the value is set to **True**, a play/pause button is shown on the video.</span></span> <span data-ttu-id="e66ae-168">如果此值设置为 **False**，将不显示播放/暂停按钮，当用户仍然可以使用键盘暂停和恢复播放视频。</span><span class="sxs-lookup"><span data-stu-id="e66ae-168">If the value is set to **False**, the play/pause button isn't shown, but users can still pause and resume the video by using the keyboard.</span></span> |
| <span data-ttu-id="e66ae-169">全屏播放</span><span class="sxs-lookup"><span data-stu-id="e66ae-169">Play fullscreen</span></span>       | <span data-ttu-id="e66ae-170">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e66ae-170">**True** or **False**</span></span>               | <span data-ttu-id="e66ae-171">如果此值设置为 **True**，将以全屏模式播放视频。</span><span class="sxs-lookup"><span data-stu-id="e66ae-171">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="e66ae-172">控件</span><span class="sxs-lookup"><span data-stu-id="e66ae-172">Controls</span></span>              | <span data-ttu-id="e66ae-173">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e66ae-173">**True** or **False**</span></span>               | <span data-ttu-id="e66ae-174">如果此值设置为 **True**，将显示所有控件。</span><span class="sxs-lookup"><span data-stu-id="e66ae-174">When the value is set to **True**, all controls are shown.</span></span> <span data-ttu-id="e66ae-175">这些控件包括播放和暂停按钮、进度指示器和隐藏式字幕。</span><span class="sxs-lookup"><span data-stu-id="e66ae-175">These controls include play and pause buttons, a progress indicator, and closed captions.</span></span> |
| <span data-ttu-id="e66ae-176">隐藏海报框架</span><span class="sxs-lookup"><span data-stu-id="e66ae-176">Hide poster frame</span></span>     | <span data-ttu-id="e66ae-177">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="e66ae-177">**True** or **False**</span></span>               | <span data-ttu-id="e66ae-178">视频可具有海报框架。</span><span class="sxs-lookup"><span data-stu-id="e66ae-178">A video can have a poster frame.</span></span> <span data-ttu-id="e66ae-179">如果此属性的值设置为 **True**，将隐藏海报框架。</span><span class="sxs-lookup"><span data-stu-id="e66ae-179">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="e66ae-180">蒙板级别</span><span class="sxs-lookup"><span data-stu-id="e66ae-180">Mask level</span></span>            | <span data-ttu-id="e66ae-181">从 **0** 到 **100** 的数字</span><span class="sxs-lookup"><span data-stu-id="e66ae-181">A number from **0** through **100**</span></span> | <span data-ttu-id="e66ae-182">为风格而向视频应用的蒙板。</span><span class="sxs-lookup"><span data-stu-id="e66ae-182">The mask that is applied to the video for styling.</span></span> |
| <span data-ttu-id="e66ae-183">全屏图标样式</span><span class="sxs-lookup"><span data-stu-id="e66ae-183">Fullscreen icon style</span></span> | <span data-ttu-id="e66ae-184">**正方形**或**箭头**</span><span class="sxs-lookup"><span data-stu-id="e66ae-184">**Square** or **Arrow**</span></span>             | <span data-ttu-id="e66ae-185">视频播放器中显示的全屏图标的样式。</span><span class="sxs-lookup"><span data-stu-id="e66ae-185">The style of the full-screen icon that is shown in the video player.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="e66ae-186">向页面添加视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="e66ae-186">Add a video player module to a page</span></span>

<span data-ttu-id="e66ae-187">若要向新页面添加视频播放器模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="e66ae-187">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e66ae-188">创建一个名称为**视频播放器模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="e66ae-188">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="e66ae-189">在默认页的**主**插槽中，添加一个容器模块。</span><span class="sxs-lookup"><span data-stu-id="e66ae-189">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="e66ae-190">在容器模块中，添加视频播放器模块和氛围视频播放器模块。</span><span class="sxs-lookup"><span data-stu-id="e66ae-190">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="e66ae-191">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="e66ae-191">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="e66ae-192">使用您刚才创建的视频播放器模板创建一个名称为**视频播放器页**的页面。</span><span class="sxs-lookup"><span data-stu-id="e66ae-192">Use the video player template that you just created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="e66ae-193">在新页的**主**插槽中，添加一个氛围视频播放器模块。</span><span class="sxs-lookup"><span data-stu-id="e66ae-193">In the **Main** slot of the new page, add an ambient video player module.</span></span>
1. <span data-ttu-id="e66ae-194">在氛围视频播放器模块的设置中，转到**媒体**，然后上传一个视频文件。</span><span class="sxs-lookup"><span data-stu-id="e66ae-194">In the settings for the ambient video player module, go to **Media**, and upload a video file.</span></span> <span data-ttu-id="e66ae-195">可以根据需要更改**自动播放**、**循环**等属性。</span><span class="sxs-lookup"><span data-stu-id="e66ae-195">You can change the **Autoplay**, **Loop**, and other properties as you require.</span></span>
1. <span data-ttu-id="e66ae-196">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="e66ae-196">Save and preview the page.</span></span>
1. <span data-ttu-id="e66ae-197">在新页的**主**插槽中，添加一个视频播放器模块。</span><span class="sxs-lookup"><span data-stu-id="e66ae-197">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="e66ae-198">在视频播放器模块的设置中，转到**媒体**，然后上传一个视频文件。</span><span class="sxs-lookup"><span data-stu-id="e66ae-198">In the settings for the video player module, go to **Media**, and upload a video file.</span></span>
1. <span data-ttu-id="e66ae-199">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="e66ae-199">Save and preview the page.</span></span> <span data-ttu-id="e66ae-200">应该可以在页面中看到这两个视频模块。</span><span class="sxs-lookup"><span data-stu-id="e66ae-200">You should see both video modules on the page.</span></span> <span data-ttu-id="e66ae-201">可以更改更多属性以自定义各模块的行为。</span><span class="sxs-lookup"><span data-stu-id="e66ae-201">You can change additional settings to customize the behavior of each module.</span></span>
1. <span data-ttu-id="e66ae-202">签入页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="e66ae-202">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e66ae-203">其他资源</span><span class="sxs-lookup"><span data-stu-id="e66ae-203">Additional resources</span></span>

[<span data-ttu-id="e66ae-204">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="e66ae-204">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e66ae-205">预警模块</span><span class="sxs-lookup"><span data-stu-id="e66ae-205">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="e66ae-206">传送模块</span><span class="sxs-lookup"><span data-stu-id="e66ae-206">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="e66ae-207">内容丰富块模块</span><span class="sxs-lookup"><span data-stu-id="e66ae-207">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="e66ae-208">内容放置模块</span><span class="sxs-lookup"><span data-stu-id="e66ae-208">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="e66ae-209">特色模块</span><span class="sxs-lookup"><span data-stu-id="e66ae-209">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="e66ae-210">主图模块</span><span class="sxs-lookup"><span data-stu-id="e66ae-210">Hero module</span></span>](add-hero-module.md)
