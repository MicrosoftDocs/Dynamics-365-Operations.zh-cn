---
title: 上传非图像和视频文件
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传非图像和视频的二进制文件。
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3392f5f36d04e8cb0a9d6e6b7db31ff62c987649
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995762"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="93c16-103">上传非图像和视频文件</span><span class="sxs-lookup"><span data-stu-id="93c16-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="93c16-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传非图像和视频文件。</span><span class="sxs-lookup"><span data-stu-id="93c16-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="93c16-105">概览</span><span class="sxs-lookup"><span data-stu-id="93c16-105">Overview</span></span>

<span data-ttu-id="93c16-106">Commerce 站点构建器的媒体库支持上传非图像或视频的二进制资产。</span><span class="sxs-lookup"><span data-stu-id="93c16-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="93c16-107">例如，可以上传 Microsoft Excel、Microsoft Word、Microsoft PowerPoint 或 PDF 文件。</span><span class="sxs-lookup"><span data-stu-id="93c16-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="93c16-108">支持以下文档类型：</span><span class="sxs-lookup"><span data-stu-id="93c16-108">The following document types are supported:</span></span>
- <span data-ttu-id="93c16-109">7Z</span><span class="sxs-lookup"><span data-stu-id="93c16-109">7Z</span></span>
- <span data-ttu-id="93c16-110">AVI</span><span class="sxs-lookup"><span data-stu-id="93c16-110">AVI</span></span>
- <span data-ttu-id="93c16-111">CS</span><span class="sxs-lookup"><span data-stu-id="93c16-111">CS</span></span>
- <span data-ttu-id="93c16-112">CSS</span><span class="sxs-lookup"><span data-stu-id="93c16-112">CSS</span></span>
- <span data-ttu-id="93c16-113">DOC</span><span class="sxs-lookup"><span data-stu-id="93c16-113">DOC</span></span>
- <span data-ttu-id="93c16-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="93c16-114">DOCX</span></span>
- <span data-ttu-id="93c16-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="93c16-115">EPUB</span></span>
- <span data-ttu-id="93c16-116">GIF</span><span class="sxs-lookup"><span data-stu-id="93c16-116">GIF</span></span>
- <span data-ttu-id="93c16-117">INDD</span><span class="sxs-lookup"><span data-stu-id="93c16-117">INDD</span></span>
- <span data-ttu-id="93c16-118">JAR</span><span class="sxs-lookup"><span data-stu-id="93c16-118">JAR</span></span>
- <span data-ttu-id="93c16-119">JPG</span><span class="sxs-lookup"><span data-stu-id="93c16-119">JPG</span></span>
- <span data-ttu-id="93c16-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="93c16-120">JPEG</span></span>
- <span data-ttu-id="93c16-121">JS</span><span class="sxs-lookup"><span data-stu-id="93c16-121">JS</span></span>
- <span data-ttu-id="93c16-122">MP3</span><span class="sxs-lookup"><span data-stu-id="93c16-122">MP3</span></span>
- <span data-ttu-id="93c16-123">MP4</span><span class="sxs-lookup"><span data-stu-id="93c16-123">MP4</span></span>
- <span data-ttu-id="93c16-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="93c16-124">MPEG</span></span>
- <span data-ttu-id="93c16-125">MPG</span><span class="sxs-lookup"><span data-stu-id="93c16-125">MPG</span></span>
- <span data-ttu-id="93c16-126">ODP</span><span class="sxs-lookup"><span data-stu-id="93c16-126">ODP</span></span>
- <span data-ttu-id="93c16-127">ODS</span><span class="sxs-lookup"><span data-stu-id="93c16-127">ODS</span></span>
- <span data-ttu-id="93c16-128">ODT</span><span class="sxs-lookup"><span data-stu-id="93c16-128">ODT</span></span>
- <span data-ttu-id="93c16-129">PDF</span><span class="sxs-lookup"><span data-stu-id="93c16-129">PDF</span></span>
- <span data-ttu-id="93c16-130">PNG</span><span class="sxs-lookup"><span data-stu-id="93c16-130">PNG</span></span>
- <span data-ttu-id="93c16-131">PPT</span><span class="sxs-lookup"><span data-stu-id="93c16-131">PPT</span></span>
- <span data-ttu-id="93c16-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="93c16-132">PPTX</span></span>
- <span data-ttu-id="93c16-133">PS</span><span class="sxs-lookup"><span data-stu-id="93c16-133">PS</span></span>
- <span data-ttu-id="93c16-134">QXP</span><span class="sxs-lookup"><span data-stu-id="93c16-134">QXP</span></span>
- <span data-ttu-id="93c16-135">RAR</span><span class="sxs-lookup"><span data-stu-id="93c16-135">RAR</span></span>
- <span data-ttu-id="93c16-136">RTF</span><span class="sxs-lookup"><span data-stu-id="93c16-136">RTF</span></span>
- <span data-ttu-id="93c16-137">SVG</span><span class="sxs-lookup"><span data-stu-id="93c16-137">SVG</span></span>
- <span data-ttu-id="93c16-138">TAR</span><span class="sxs-lookup"><span data-stu-id="93c16-138">TAR</span></span>
- <span data-ttu-id="93c16-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="93c16-139">TGZ</span></span>
- <span data-ttu-id="93c16-140">TXT</span><span class="sxs-lookup"><span data-stu-id="93c16-140">TXT</span></span>
- <span data-ttu-id="93c16-141">WMV</span><span class="sxs-lookup"><span data-stu-id="93c16-141">WMV</span></span>
- <span data-ttu-id="93c16-142">XLS</span><span class="sxs-lookup"><span data-stu-id="93c16-142">XLS</span></span>
- <span data-ttu-id="93c16-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="93c16-143">XLSX</span></span>
- <span data-ttu-id="93c16-144">XML</span><span class="sxs-lookup"><span data-stu-id="93c16-144">XML</span></span>
- <span data-ttu-id="93c16-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="93c16-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="93c16-146">上载文件</span><span class="sxs-lookup"><span data-stu-id="93c16-146">Upload a file</span></span>

<span data-ttu-id="93c16-147">要将文件上传到 Commerce 站点构建器，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="93c16-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="93c16-148">在左侧导航窗格中，选择 **媒体库**。</span><span class="sxs-lookup"><span data-stu-id="93c16-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="93c16-149">在命令栏上，选择 **上传 \> 上传媒体项**。</span><span class="sxs-lookup"><span data-stu-id="93c16-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="93c16-150">在文件资源管理器中，选择一个或多个文件，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="93c16-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="93c16-151">根据需要在 **上传媒体项** 对话框中输入标题、描述和关键字元数据。</span><span class="sxs-lookup"><span data-stu-id="93c16-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="93c16-152">若要在上传后立即发布文件，请选中 **上传后发布媒体项** 复选框。</span><span class="sxs-lookup"><span data-stu-id="93c16-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="93c16-153">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="93c16-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93c16-154">其他资源</span><span class="sxs-lookup"><span data-stu-id="93c16-154">Additional resources</span></span>

[<span data-ttu-id="93c16-155">数字资产管理概览</span><span class="sxs-lookup"><span data-stu-id="93c16-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="93c16-156">上传图像</span><span class="sxs-lookup"><span data-stu-id="93c16-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="93c16-157">上传视频</span><span class="sxs-lookup"><span data-stu-id="93c16-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="93c16-158">裁剪图像</span><span class="sxs-lookup"><span data-stu-id="93c16-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="93c16-159">自定义图像焦点</span><span class="sxs-lookup"><span data-stu-id="93c16-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="93c16-160">上传和提供静态文件</span><span class="sxs-lookup"><span data-stu-id="93c16-160">Upload and serve static files</span></span>](upload-serve-static-files.md)
