---
title: 视频播放器模块
description: 此主题介绍视频播放器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 13072c8d6839fef1ab0dd55d626c23a2a1084d4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209171"
---
# <a name="video-player-module"></a><span data-ttu-id="3f0f2-103">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="3f0f2-103">Video player module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f0f2-104">此主题介绍视频播放器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3f0f2-105">视频播放器模块用于支持视频播放。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-105">The video player module is used to support video playback.</span></span> <span data-ttu-id="3f0f2-106">只要视频内容已上传到内容管理系统 (CMS) 并在其中可用，就可以将它添加到任何页面。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-106">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="3f0f2-107">视频播放器模块支持 .mp4 媒体类型。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-107">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="3f0f2-108">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="3f0f2-108">Video player module</span></span>

<span data-ttu-id="3f0f2-109">可在电子商务站点中使用视频播放器模块展示视频。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-109">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="3f0f2-110">它支持所有播放功能，如播放、暂停、全屏模式、音频描述和隐藏式字幕。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-110">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="3f0f2-111">视频播放器模块还支持自定义隐藏式字幕以满足 Microsoft 的辅助功能标准。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-111">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="3f0f2-112">例如，可自定义字体大小和背景色。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-112">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="3f0f2-113">视频播放器模块还支持辅助音轨。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-113">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="3f0f2-114">将视频上载到 CMS 后，还可以上载辅助音轨。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-114">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="3f0f2-115">然后，如果用户选择了视频播放器模块，它则可以播放辅助音轨。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-115">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="3f0f2-116">电子商务中的视频播放器模块示例</span><span class="sxs-lookup"><span data-stu-id="3f0f2-116">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="3f0f2-117">产品详细信息页或市场营销页上的说明性视频</span><span class="sxs-lookup"><span data-stu-id="3f0f2-117">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="3f0f2-118">任何市场营销页上的促销视频或有关政策的视频</span><span class="sxs-lookup"><span data-stu-id="3f0f2-118">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="3f0f2-119">产品详细信息页或市场营销页上重点介绍产品特色的市场营销视频</span><span class="sxs-lookup"><span data-stu-id="3f0f2-119">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

<span data-ttu-id="3f0f2-120">下图显示了主页上的视频播放器模块的示例。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-120">The following image shows an example of a video player module on a home page.</span></span>

![视频播放器模块示例](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a><span data-ttu-id="3f0f2-122">视频播放器模块属性</span><span class="sxs-lookup"><span data-stu-id="3f0f2-122">Video player module properties</span></span>

| <span data-ttu-id="3f0f2-123">属性名称</span><span class="sxs-lookup"><span data-stu-id="3f0f2-123">Property name</span></span>         | <span data-ttu-id="3f0f2-124">值</span><span class="sxs-lookup"><span data-stu-id="3f0f2-124">Value</span></span>                               | <span data-ttu-id="3f0f2-125">说明</span><span class="sxs-lookup"><span data-stu-id="3f0f2-125">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="3f0f2-126">自动播放</span><span class="sxs-lookup"><span data-stu-id="3f0f2-126">Auto play</span></span>             | <span data-ttu-id="3f0f2-127">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="3f0f2-127">**True** or **False**</span></span>               | <span data-ttu-id="3f0f2-128">如果此值设置为 **True**，将自动播放视频。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-128">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="3f0f2-129">静音</span><span class="sxs-lookup"><span data-stu-id="3f0f2-129">Mute</span></span>                  | <span data-ttu-id="3f0f2-130">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="3f0f2-130">**True** or **False**</span></span>               | <span data-ttu-id="3f0f2-131">如果此值设置为 **True**，将静音。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-131">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="3f0f2-132">对于此播放器，默认值为 **False**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-132">For this player, the default value is **False**.</span></span> <span data-ttu-id="3f0f2-133">在 Chrome 浏览器中，自动播放的视频默认静音，仅当用户手动播放视频时，才播放音频。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-133">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="3f0f2-134">循环</span><span class="sxs-lookup"><span data-stu-id="3f0f2-134">Loop</span></span>                  | <span data-ttu-id="3f0f2-135">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="3f0f2-135">**True** or **False**</span></span>               | <span data-ttu-id="3f0f2-136">如果此值设置为 **True**，将循环重复播放视频。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-136">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="3f0f2-137">媒体</span><span class="sxs-lookup"><span data-stu-id="3f0f2-137">Media</span></span>                 | <span data-ttu-id="3f0f2-138">视频文件路径和名称</span><span class="sxs-lookup"><span data-stu-id="3f0f2-138">Video file path and name</span></span> | <span data-ttu-id="3f0f2-139">视频播放器中播放的视频文件。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-139">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="3f0f2-140">全屏播放</span><span class="sxs-lookup"><span data-stu-id="3f0f2-140">Play fullscreen</span></span>       | <span data-ttu-id="3f0f2-141">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="3f0f2-141">**True** or **False**</span></span>               | <span data-ttu-id="3f0f2-142">如果此值设置为 **True**，将以全屏模式播放视频。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-142">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="3f0f2-143">播放暂停触发器</span><span class="sxs-lookup"><span data-stu-id="3f0f2-143">Play pause trigger</span></span>    | <span data-ttu-id="3f0f2-144">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="3f0f2-144">**True** or **False**</span></span>               | <span data-ttu-id="3f0f2-145">如果此值设置为 **True**，视频中将显示播放/暂停按钮。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-145">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="3f0f2-146">视频播放器控件</span><span class="sxs-lookup"><span data-stu-id="3f0f2-146">Video player controls</span></span> | <span data-ttu-id="3f0f2-147">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="3f0f2-147">**True** or **False**</span></span>               | <span data-ttu-id="3f0f2-148">如果此值设置为 **True**，将显示所有视频播放器控件。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-148">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="3f0f2-149">这些控件包括播放和暂停按钮、进度指示器和隐藏式字幕选项。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-149">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="3f0f2-150">隐藏海报图像</span><span class="sxs-lookup"><span data-stu-id="3f0f2-150">Hide poster image</span></span>     | <span data-ttu-id="3f0f2-151">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="3f0f2-151">**True** or **False**</span></span>               | <span data-ttu-id="3f0f2-152">视频可具有海报框架。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-152">A video can have a poster frame.</span></span> <span data-ttu-id="3f0f2-153">如果此属性的值设置为 **True**，将隐藏海报框架。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-153">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="3f0f2-154">蒙板级别</span><span class="sxs-lookup"><span data-stu-id="3f0f2-154">Mask level</span></span>            | <span data-ttu-id="3f0f2-155">从 **0** 到 **100** 的数字</span><span class="sxs-lookup"><span data-stu-id="3f0f2-155">A number from **0** through **100**</span></span> | <span data-ttu-id="3f0f2-156">为风格而向视频应用的蒙板。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-156">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="3f0f2-157">向页面添加视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="3f0f2-157">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="3f0f2-158">在创建视频播放器模块之前，必须首先将视频上传到媒体库。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-158">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="3f0f2-159">若要向新页面添加视频播放器模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-159">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3f0f2-160">转到 **模板**，选择 **新建** 创建新模板。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="3f0f2-161">在 **新建模板** 对话框的 **模板名称** 下，输入 **视频播放器模板**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-161">In the **New Template** dialog box, under **Template name**, enter **Video player template**, and then select **OK**.</span></span>
1. <span data-ttu-id="3f0f2-162">在 **正文** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-162">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3f0f2-163">在 **添加模块** 对话框中，选择 **默认页面** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-163">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3f0f2-164">在 **默认页** 模块的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-164">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3f0f2-165">在 **添加模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-165">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3f0f2-166">在 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-166">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3f0f2-167">在 **添加模块** 对话框中，选择 **视频播放器模板** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-167">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3f0f2-168">选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-168">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="3f0f2-169">转到 **页面**，选择 **新建** 创建新页面。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-169">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="3f0f2-170">在 **选择模板** 对话框中，选择您创建的视频播放器模板。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-170">In the **Choose a template** dialog box, select the video player template that you created.</span></span> <span data-ttu-id="3f0f2-171">在 **页面名称** 下，输入 **视频播放器页面**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-171">Under **Page name**, enter **Video player page**, and then select **OK**.</span></span>
1. <span data-ttu-id="3f0f2-172">在新页面的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-172">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3f0f2-173">在 **添加模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-173">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3f0f2-174">在 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-174">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3f0f2-175">在 **添加模块** 对话框中，选择 **视频播放器模板** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-175">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3f0f2-176">在视频播放器模块的属性窗格中，选择 **添加视频**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-176">In the property pane of the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="3f0f2-177">在 **媒体选择器** 对话框中，选择一个视频，然后选择 **上载新媒体项目**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-177">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="3f0f2-178">在文件资源管理器中，选择一个视频文件，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-178">In File Explorer, select a video file, and then select **Open**.</span></span>
1. <span data-ttu-id="3f0f2-179">在 **上传媒体项** 对话框中，根据需要输入标题和其他信息，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-179">In the **Upload Media Item** dialog box, enter a title and other information as needed, and then select **OK**.</span></span>
1. <span data-ttu-id="3f0f2-180">在 **媒体选择器** 对话框中，选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-180">In the **Media Picker** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="3f0f2-181">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-181">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="3f0f2-182">应该可以在页面中看到此视频模块。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-182">You should see the video module on the page.</span></span> <span data-ttu-id="3f0f2-183">可以更改更多属性以自定义模块的行为。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-183">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="3f0f2-184">选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="3f0f2-184">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="3f0f2-185">其他资源</span><span class="sxs-lookup"><span data-stu-id="3f0f2-185">Additional resources</span></span>

[<span data-ttu-id="3f0f2-186">模块库概述</span><span class="sxs-lookup"><span data-stu-id="3f0f2-186">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3f0f2-187">促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="3f0f2-187">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="3f0f2-188">传送模块</span><span class="sxs-lookup"><span data-stu-id="3f0f2-188">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="3f0f2-189">文本块模块</span><span class="sxs-lookup"><span data-stu-id="3f0f2-189">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="3f0f2-190">内容块模块</span><span class="sxs-lookup"><span data-stu-id="3f0f2-190">Content block module</span></span>](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]