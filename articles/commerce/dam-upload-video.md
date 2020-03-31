---
title: 上传视频
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传视频。
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 98cb4f9049509dd700cf38a5d176447f86e9c824
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096979"
---
# <a name="upload-videos"></a><span data-ttu-id="cbeeb-103">上传视频</span><span class="sxs-lookup"><span data-stu-id="cbeeb-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cbeeb-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传视频。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="cbeeb-105">概览</span><span class="sxs-lookup"><span data-stu-id="cbeeb-105">Overview</span></span>

<span data-ttu-id="cbeeb-106">Commerce 站点构建器的媒体库允许上传视频。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="cbeeb-107">应始终上传比特率和分辨率最高的视频版本，因为将把视频自动转换为适合不同视区及其断点的视频。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="cbeeb-108">上传期间指定的视频信息</span><span class="sxs-lookup"><span data-stu-id="cbeeb-108">Video information specified during upload</span></span>

<span data-ttu-id="cbeeb-109">上载视频时，可以指定以下信息。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="cbeeb-110">**标题、描述、关键字**：视频的元数据。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="cbeeb-111">**自动生成隐藏式字幕**：指定应该为视频自动生成隐藏式字幕。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="cbeeb-112">**隐藏式字幕**：指定要使用的隐藏式字幕。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="cbeeb-113">**常规音频**：指定要使用的常规音轨。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="cbeeb-114">**缩略图**：指定视频的缩略图。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="cbeeb-115">如果不指定，将自动生成。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="cbeeb-116">**描述性音频**：指定要使用的描述性音轨。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="cbeeb-117">上传视频</span><span class="sxs-lookup"><span data-stu-id="cbeeb-117">Upload a video</span></span>

<span data-ttu-id="cbeeb-118">若要在站点构建器中上传视频，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cbeeb-119">在左侧导航窗格中，选择**媒体库**。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="cbeeb-120">在命令栏上，选择**上传 \> 上传媒体项**。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="cbeeb-121">在文件资源管理器中，浏览到要上传的一个或多个视频文件并选中，然后选择**打开**。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="cbeeb-122">在**上传媒体项**对话框中，输入必需的标题和替代文本。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="cbeeb-123">如果需要，输入可选描述和关键字，然后选择类别。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="cbeeb-124">如果要在上传后立即发布视频，请选中**上传后发布媒体项**复选框</span><span class="sxs-lookup"><span data-stu-id="cbeeb-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="cbeeb-125">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-125">Select **OK**.</span></span>

<span data-ttu-id="cbeeb-126">如果要同时上传多种资产（例如，图像和视频），则在**上传媒体项**对话框中只能指定关键字，是否应该在上传后立即发布文件，以及是否应该为视频自动生成隐藏式字幕。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="cbeeb-127">所有资产将共享相同的关键字。</span><span class="sxs-lookup"><span data-stu-id="cbeeb-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cbeeb-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="cbeeb-128">Additional resources</span></span>

[<span data-ttu-id="cbeeb-129">数字资产管理概览</span><span class="sxs-lookup"><span data-stu-id="cbeeb-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="cbeeb-130">上传图像</span><span class="sxs-lookup"><span data-stu-id="cbeeb-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="cbeeb-131">上传文件</span><span class="sxs-lookup"><span data-stu-id="cbeeb-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="cbeeb-132">裁剪图像</span><span class="sxs-lookup"><span data-stu-id="cbeeb-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="cbeeb-133">自定义图像焦点</span><span class="sxs-lookup"><span data-stu-id="cbeeb-133">Customize image focal points</span></span>](dam-custom-focal-point.md)