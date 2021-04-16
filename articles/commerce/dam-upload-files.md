---
title: 上传非图像和视频文件
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传非图像和视频的二进制文件。
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
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799245"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="c277d-103">上传图像和视频以外的文件</span><span class="sxs-lookup"><span data-stu-id="c277d-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c277d-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传非图像和视频的文件。</span><span class="sxs-lookup"><span data-stu-id="c277d-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="c277d-105">Commerce 站点构建器的媒体库支持上传非图像或视频的二进制资产。</span><span class="sxs-lookup"><span data-stu-id="c277d-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="c277d-106">例如，可以上传 Microsoft Excel、Microsoft Word、Microsoft PowerPoint 或 PDF 文件。</span><span class="sxs-lookup"><span data-stu-id="c277d-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="c277d-107">支持以下文档类型：</span><span class="sxs-lookup"><span data-stu-id="c277d-107">The following document types are supported:</span></span>
- <span data-ttu-id="c277d-108">7Z</span><span class="sxs-lookup"><span data-stu-id="c277d-108">7Z</span></span>
- <span data-ttu-id="c277d-109">AVI</span><span class="sxs-lookup"><span data-stu-id="c277d-109">AVI</span></span>
- <span data-ttu-id="c277d-110">CS</span><span class="sxs-lookup"><span data-stu-id="c277d-110">CS</span></span>
- <span data-ttu-id="c277d-111">CSS</span><span class="sxs-lookup"><span data-stu-id="c277d-111">CSS</span></span>
- <span data-ttu-id="c277d-112">DOC</span><span class="sxs-lookup"><span data-stu-id="c277d-112">DOC</span></span>
- <span data-ttu-id="c277d-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="c277d-113">DOCX</span></span>
- <span data-ttu-id="c277d-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="c277d-114">EPUB</span></span>
- <span data-ttu-id="c277d-115">GIF</span><span class="sxs-lookup"><span data-stu-id="c277d-115">GIF</span></span>
- <span data-ttu-id="c277d-116">INDD</span><span class="sxs-lookup"><span data-stu-id="c277d-116">INDD</span></span>
- <span data-ttu-id="c277d-117">JAR</span><span class="sxs-lookup"><span data-stu-id="c277d-117">JAR</span></span>
- <span data-ttu-id="c277d-118">JPG</span><span class="sxs-lookup"><span data-stu-id="c277d-118">JPG</span></span>
- <span data-ttu-id="c277d-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="c277d-119">JPEG</span></span>
- <span data-ttu-id="c277d-120">JS</span><span class="sxs-lookup"><span data-stu-id="c277d-120">JS</span></span>
- <span data-ttu-id="c277d-121">MP3</span><span class="sxs-lookup"><span data-stu-id="c277d-121">MP3</span></span>
- <span data-ttu-id="c277d-122">MP4</span><span class="sxs-lookup"><span data-stu-id="c277d-122">MP4</span></span>
- <span data-ttu-id="c277d-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="c277d-123">MPEG</span></span>
- <span data-ttu-id="c277d-124">MPG</span><span class="sxs-lookup"><span data-stu-id="c277d-124">MPG</span></span>
- <span data-ttu-id="c277d-125">ODP</span><span class="sxs-lookup"><span data-stu-id="c277d-125">ODP</span></span>
- <span data-ttu-id="c277d-126">ODS</span><span class="sxs-lookup"><span data-stu-id="c277d-126">ODS</span></span>
- <span data-ttu-id="c277d-127">ODT</span><span class="sxs-lookup"><span data-stu-id="c277d-127">ODT</span></span>
- <span data-ttu-id="c277d-128">PDF</span><span class="sxs-lookup"><span data-stu-id="c277d-128">PDF</span></span>
- <span data-ttu-id="c277d-129">PNG</span><span class="sxs-lookup"><span data-stu-id="c277d-129">PNG</span></span>
- <span data-ttu-id="c277d-130">PPT</span><span class="sxs-lookup"><span data-stu-id="c277d-130">PPT</span></span>
- <span data-ttu-id="c277d-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="c277d-131">PPTX</span></span>
- <span data-ttu-id="c277d-132">PS</span><span class="sxs-lookup"><span data-stu-id="c277d-132">PS</span></span>
- <span data-ttu-id="c277d-133">QXP</span><span class="sxs-lookup"><span data-stu-id="c277d-133">QXP</span></span>
- <span data-ttu-id="c277d-134">RAR</span><span class="sxs-lookup"><span data-stu-id="c277d-134">RAR</span></span>
- <span data-ttu-id="c277d-135">RTF</span><span class="sxs-lookup"><span data-stu-id="c277d-135">RTF</span></span>
- <span data-ttu-id="c277d-136">SVG</span><span class="sxs-lookup"><span data-stu-id="c277d-136">SVG</span></span>
- <span data-ttu-id="c277d-137">TAR</span><span class="sxs-lookup"><span data-stu-id="c277d-137">TAR</span></span>
- <span data-ttu-id="c277d-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="c277d-138">TGZ</span></span>
- <span data-ttu-id="c277d-139">TXT</span><span class="sxs-lookup"><span data-stu-id="c277d-139">TXT</span></span>
- <span data-ttu-id="c277d-140">WMV</span><span class="sxs-lookup"><span data-stu-id="c277d-140">WMV</span></span>
- <span data-ttu-id="c277d-141">XLS</span><span class="sxs-lookup"><span data-stu-id="c277d-141">XLS</span></span>
- <span data-ttu-id="c277d-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="c277d-142">XLSX</span></span>
- <span data-ttu-id="c277d-143">XML</span><span class="sxs-lookup"><span data-stu-id="c277d-143">XML</span></span>
- <span data-ttu-id="c277d-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="c277d-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="c277d-145">上载文件</span><span class="sxs-lookup"><span data-stu-id="c277d-145">Upload a file</span></span>

<span data-ttu-id="c277d-146">要将文件上传到 Commerce 站点构建器，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c277d-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c277d-147">在左侧导航窗格中，选择 **媒体库**。</span><span class="sxs-lookup"><span data-stu-id="c277d-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="c277d-148">在命令栏上，选择 **上传 \> 上传媒体项**。</span><span class="sxs-lookup"><span data-stu-id="c277d-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="c277d-149">在文件资源管理器中，选择一个或多个文件，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="c277d-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="c277d-150">根据需要在 **上传媒体项** 对话框中输入标题、描述和关键字元数据。</span><span class="sxs-lookup"><span data-stu-id="c277d-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="c277d-151">若要在上传后立即发布文件，请选中 **上传后发布媒体项** 复选框。</span><span class="sxs-lookup"><span data-stu-id="c277d-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="c277d-152">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c277d-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c277d-153">其他资源</span><span class="sxs-lookup"><span data-stu-id="c277d-153">Additional resources</span></span>

[<span data-ttu-id="c277d-154">数字资产管理概览</span><span class="sxs-lookup"><span data-stu-id="c277d-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="c277d-155">上传图像</span><span class="sxs-lookup"><span data-stu-id="c277d-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="c277d-156">上传视频</span><span class="sxs-lookup"><span data-stu-id="c277d-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="c277d-157">裁剪图像</span><span class="sxs-lookup"><span data-stu-id="c277d-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="c277d-158">自定义图像焦点</span><span class="sxs-lookup"><span data-stu-id="c277d-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="c277d-159">上传和提供静态文件</span><span class="sxs-lookup"><span data-stu-id="c277d-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
