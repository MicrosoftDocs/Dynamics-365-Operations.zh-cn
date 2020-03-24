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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fc0490e3532dcbb9c1e91101009b2d4605315416
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096976"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="fc7e3-103">上传非图像和视频文件</span><span class="sxs-lookup"><span data-stu-id="fc7e3-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc7e3-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传非图像和视频文件。</span><span class="sxs-lookup"><span data-stu-id="fc7e3-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="fc7e3-105">概览</span><span class="sxs-lookup"><span data-stu-id="fc7e3-105">Overview</span></span>

<span data-ttu-id="fc7e3-106">Commerce 站点构建器的媒体库支持上传非图像或视频的二进制资产。</span><span class="sxs-lookup"><span data-stu-id="fc7e3-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="fc7e3-107">例如，可以上传 Microsoft Excel、Microsoft Word、Microsoft PowerPoint 或 PDF 文件。</span><span class="sxs-lookup"><span data-stu-id="fc7e3-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="fc7e3-108">支持以下文档类型：</span><span class="sxs-lookup"><span data-stu-id="fc7e3-108">The following document types are supported:</span></span>
- <span data-ttu-id="fc7e3-109">7Z</span><span class="sxs-lookup"><span data-stu-id="fc7e3-109">7Z</span></span>
- <span data-ttu-id="fc7e3-110">AVI</span><span class="sxs-lookup"><span data-stu-id="fc7e3-110">AVI</span></span>
- <span data-ttu-id="fc7e3-111">CS</span><span class="sxs-lookup"><span data-stu-id="fc7e3-111">CS</span></span>
- <span data-ttu-id="fc7e3-112">CSS</span><span class="sxs-lookup"><span data-stu-id="fc7e3-112">CSS</span></span>
- <span data-ttu-id="fc7e3-113">DOC</span><span class="sxs-lookup"><span data-stu-id="fc7e3-113">DOC</span></span>
- <span data-ttu-id="fc7e3-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="fc7e3-114">DOCX</span></span>
- <span data-ttu-id="fc7e3-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="fc7e3-115">EPUB</span></span>
- <span data-ttu-id="fc7e3-116">GIF</span><span class="sxs-lookup"><span data-stu-id="fc7e3-116">GIF</span></span>
- <span data-ttu-id="fc7e3-117">INDD</span><span class="sxs-lookup"><span data-stu-id="fc7e3-117">INDD</span></span>
- <span data-ttu-id="fc7e3-118">JAR</span><span class="sxs-lookup"><span data-stu-id="fc7e3-118">JAR</span></span>
- <span data-ttu-id="fc7e3-119">JPG</span><span class="sxs-lookup"><span data-stu-id="fc7e3-119">JPG</span></span>
- <span data-ttu-id="fc7e3-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="fc7e3-120">JPEG</span></span>
- <span data-ttu-id="fc7e3-121">JS</span><span class="sxs-lookup"><span data-stu-id="fc7e3-121">JS</span></span>
- <span data-ttu-id="fc7e3-122">MP3</span><span class="sxs-lookup"><span data-stu-id="fc7e3-122">MP3</span></span>
- <span data-ttu-id="fc7e3-123">MP4</span><span class="sxs-lookup"><span data-stu-id="fc7e3-123">MP4</span></span>
- <span data-ttu-id="fc7e3-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="fc7e3-124">MPEG</span></span>
- <span data-ttu-id="fc7e3-125">MPG</span><span class="sxs-lookup"><span data-stu-id="fc7e3-125">MPG</span></span>
- <span data-ttu-id="fc7e3-126">ODP</span><span class="sxs-lookup"><span data-stu-id="fc7e3-126">ODP</span></span>
- <span data-ttu-id="fc7e3-127">ODS</span><span class="sxs-lookup"><span data-stu-id="fc7e3-127">ODS</span></span>
- <span data-ttu-id="fc7e3-128">ODT</span><span class="sxs-lookup"><span data-stu-id="fc7e3-128">ODT</span></span>
- <span data-ttu-id="fc7e3-129">PDF</span><span class="sxs-lookup"><span data-stu-id="fc7e3-129">PDF</span></span>
- <span data-ttu-id="fc7e3-130">PNG</span><span class="sxs-lookup"><span data-stu-id="fc7e3-130">PNG</span></span>
- <span data-ttu-id="fc7e3-131">PPT</span><span class="sxs-lookup"><span data-stu-id="fc7e3-131">PPT</span></span>
- <span data-ttu-id="fc7e3-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="fc7e3-132">PPTX</span></span>
- <span data-ttu-id="fc7e3-133">PS</span><span class="sxs-lookup"><span data-stu-id="fc7e3-133">PS</span></span>
- <span data-ttu-id="fc7e3-134">QXP</span><span class="sxs-lookup"><span data-stu-id="fc7e3-134">QXP</span></span>
- <span data-ttu-id="fc7e3-135">RAR</span><span class="sxs-lookup"><span data-stu-id="fc7e3-135">RAR</span></span>
- <span data-ttu-id="fc7e3-136">RTF</span><span class="sxs-lookup"><span data-stu-id="fc7e3-136">RTF</span></span>
- <span data-ttu-id="fc7e3-137">SVG</span><span class="sxs-lookup"><span data-stu-id="fc7e3-137">SVG</span></span>
- <span data-ttu-id="fc7e3-138">TAR</span><span class="sxs-lookup"><span data-stu-id="fc7e3-138">TAR</span></span>
- <span data-ttu-id="fc7e3-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="fc7e3-139">TGZ</span></span>
- <span data-ttu-id="fc7e3-140">TXT</span><span class="sxs-lookup"><span data-stu-id="fc7e3-140">TXT</span></span>
- <span data-ttu-id="fc7e3-141">WMV</span><span class="sxs-lookup"><span data-stu-id="fc7e3-141">WMV</span></span>
- <span data-ttu-id="fc7e3-142">XLS</span><span class="sxs-lookup"><span data-stu-id="fc7e3-142">XLS</span></span>
- <span data-ttu-id="fc7e3-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="fc7e3-143">XLSX</span></span>
- <span data-ttu-id="fc7e3-144">XML</span><span class="sxs-lookup"><span data-stu-id="fc7e3-144">XML</span></span>
- <span data-ttu-id="fc7e3-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="fc7e3-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="fc7e3-146">上载文件</span><span class="sxs-lookup"><span data-stu-id="fc7e3-146">Upload a file</span></span>

<span data-ttu-id="fc7e3-147">要将文件上传到 Commerce 站点构建器，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="fc7e3-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fc7e3-148">在左侧导航窗格中，选择**媒体库**。</span><span class="sxs-lookup"><span data-stu-id="fc7e3-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="fc7e3-149">在命令栏上，选择**上传 \> 上传媒体项**。</span><span class="sxs-lookup"><span data-stu-id="fc7e3-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="fc7e3-150">在文件资源管理器中，选择一个或多个文件，然后选择**打开**。</span><span class="sxs-lookup"><span data-stu-id="fc7e3-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="fc7e3-151">根据需要在**上传媒体项**对话框中输入标题、描述和关键字元数据。</span><span class="sxs-lookup"><span data-stu-id="fc7e3-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="fc7e3-152">若要在上传后立即发布文件，请选中**上传后发布媒体项**复选框。</span><span class="sxs-lookup"><span data-stu-id="fc7e3-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="fc7e3-153">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="fc7e3-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc7e3-154">其他资源</span><span class="sxs-lookup"><span data-stu-id="fc7e3-154">Additional resources</span></span>

[<span data-ttu-id="fc7e3-155">数字资产管理概览</span><span class="sxs-lookup"><span data-stu-id="fc7e3-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="fc7e3-156">上传图像</span><span class="sxs-lookup"><span data-stu-id="fc7e3-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="fc7e3-157">上传视频</span><span class="sxs-lookup"><span data-stu-id="fc7e3-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="fc7e3-158">裁剪图像</span><span class="sxs-lookup"><span data-stu-id="fc7e3-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="fc7e3-159">自定义图像焦点</span><span class="sxs-lookup"><span data-stu-id="fc7e3-159">Customize image focal points</span></span>](dam-custom-focal-point.md)
