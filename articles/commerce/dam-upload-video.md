---
title: 上传视频
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传视频。
author: psimolin
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5ec20f8caee2f5a62230be05923dfd52600c1e35
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799197"
---
# <a name="upload-videos"></a><span data-ttu-id="a582e-103">上传视频</span><span class="sxs-lookup"><span data-stu-id="a582e-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a582e-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传视频。</span><span class="sxs-lookup"><span data-stu-id="a582e-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="a582e-105">Commerce 站点构建器的媒体库允许上传视频。</span><span class="sxs-lookup"><span data-stu-id="a582e-105">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="a582e-106">应始终上传比特率和分辨率最高的视频版本，因为将把视频自动转换为适合不同视区及其断点的视频。</span><span class="sxs-lookup"><span data-stu-id="a582e-106">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="a582e-107">上传期间指定的视频信息</span><span class="sxs-lookup"><span data-stu-id="a582e-107">Video information specified during upload</span></span>

<span data-ttu-id="a582e-108">上载视频时，可以指定以下信息。</span><span class="sxs-lookup"><span data-stu-id="a582e-108">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="a582e-109">**标题、描述、关键字**：视频的元数据。</span><span class="sxs-lookup"><span data-stu-id="a582e-109">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="a582e-110">**自动生成隐藏式字幕**：指定应该为视频自动生成隐藏式字幕。</span><span class="sxs-lookup"><span data-stu-id="a582e-110">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="a582e-111">**隐藏式字幕**：指定要使用的隐藏式字幕。</span><span class="sxs-lookup"><span data-stu-id="a582e-111">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="a582e-112">**常规音频**：指定要使用的常规音轨。</span><span class="sxs-lookup"><span data-stu-id="a582e-112">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="a582e-113">**缩略图**：指定视频的缩略图。</span><span class="sxs-lookup"><span data-stu-id="a582e-113">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="a582e-114">如果不指定，将自动生成。</span><span class="sxs-lookup"><span data-stu-id="a582e-114">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="a582e-115">**描述性音频**：指定要使用的描述性音轨。</span><span class="sxs-lookup"><span data-stu-id="a582e-115">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="a582e-116">上传视频</span><span class="sxs-lookup"><span data-stu-id="a582e-116">Upload a video</span></span>

<span data-ttu-id="a582e-117">若要在站点构建器中上传视频，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="a582e-117">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="a582e-118">在左侧导航窗格中，选择 **媒体库**。</span><span class="sxs-lookup"><span data-stu-id="a582e-118">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="a582e-119">在命令栏上，选择 **上传 \> 上传媒体项**。</span><span class="sxs-lookup"><span data-stu-id="a582e-119">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="a582e-120">在文件资源管理器中，浏览到要上传的一个或多个视频文件并选中，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="a582e-120">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="a582e-121">在 **上传媒体项** 对话框中，输入必需的标题和替代文本。</span><span class="sxs-lookup"><span data-stu-id="a582e-121">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="a582e-122">如果需要，输入可选描述和关键字，然后选择类别。</span><span class="sxs-lookup"><span data-stu-id="a582e-122">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="a582e-123">如果要在上传后立即发布视频，请选中 **上传后发布媒体项** 复选框</span><span class="sxs-lookup"><span data-stu-id="a582e-123">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="a582e-124">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a582e-124">Select **OK**.</span></span>

<span data-ttu-id="a582e-125">如果要同时上传多种资产（例如，图像和视频），则在 **上传媒体项** 对话框中只能指定关键字，是否应该在上传后立即发布文件，以及是否应该为视频自动生成隐藏式字幕。</span><span class="sxs-lookup"><span data-stu-id="a582e-125">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="a582e-126">所有资产将共享相同的关键字。</span><span class="sxs-lookup"><span data-stu-id="a582e-126">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a582e-127">其他资源</span><span class="sxs-lookup"><span data-stu-id="a582e-127">Additional resources</span></span>

[<span data-ttu-id="a582e-128">数字资产管理概览</span><span class="sxs-lookup"><span data-stu-id="a582e-128">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="a582e-129">上传图像</span><span class="sxs-lookup"><span data-stu-id="a582e-129">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="a582e-130">上传文件</span><span class="sxs-lookup"><span data-stu-id="a582e-130">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="a582e-131">裁剪图像</span><span class="sxs-lookup"><span data-stu-id="a582e-131">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="a582e-132">自定义图像焦点</span><span class="sxs-lookup"><span data-stu-id="a582e-132">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="a582e-133">上传和提供静态文件</span><span class="sxs-lookup"><span data-stu-id="a582e-133">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
