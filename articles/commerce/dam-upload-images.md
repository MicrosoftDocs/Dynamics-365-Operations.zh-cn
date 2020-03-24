---
title: 上传图像
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传图像。
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
ms.openlocfilehash: 8571c52b98a87751400dab9482168ee370834bcc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096977"
---
# <a name="upload-images"></a><span data-ttu-id="51e0f-103">上传图像</span><span class="sxs-lookup"><span data-stu-id="51e0f-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="51e0f-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点构建器中上传图像。</span><span class="sxs-lookup"><span data-stu-id="51e0f-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="51e0f-105">概览</span><span class="sxs-lookup"><span data-stu-id="51e0f-105">Overview</span></span>

<span data-ttu-id="51e0f-106">Commerce 站点构建器的媒体库允许您上传单个图像或使用文件夹批量上传图像。</span><span class="sxs-lookup"><span data-stu-id="51e0f-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="51e0f-107">应始终上传分辨率和质量最高的图像版本，因为图像大小调整组件将针对不同视区及其断点自动优化图像。</span><span class="sxs-lookup"><span data-stu-id="51e0f-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="51e0f-108">上传期间指定的图像信息</span><span class="sxs-lookup"><span data-stu-id="51e0f-108">Image information specified during upload</span></span>

<span data-ttu-id="51e0f-109">上载图像时，可以指定以下信息。</span><span class="sxs-lookup"><span data-stu-id="51e0f-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="51e0f-110">**标题、替代文本、描述、关键字**：图像的元数据。</span><span class="sxs-lookup"><span data-stu-id="51e0f-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="51e0f-111">标题和替代文本是必需值。</span><span class="sxs-lookup"><span data-stu-id="51e0f-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="51e0f-112">**选择类别**：</span><span class="sxs-lookup"><span data-stu-id="51e0f-112">**Select category**:</span></span>
    - <span data-ttu-id="51e0f-113">**无**：用于电子商务故事分享图像。</span><span class="sxs-lookup"><span data-stu-id="51e0f-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="51e0f-114">**产品、类别、客户、员工、目录**：用于 Dynamics 365 Commerce 全渠道图像。</span><span class="sxs-lookup"><span data-stu-id="51e0f-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="51e0f-115">**上传后发布资产**：如果选中此复选框，图像在上传后将立即发布。</span><span class="sxs-lookup"><span data-stu-id="51e0f-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="51e0f-116">还将对已分配了类别的图像资产使用该类别作为关键字进行标记，以便帮助搜索特定类别的资产。</span><span class="sxs-lookup"><span data-stu-id="51e0f-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="51e0f-117">全渠道图像的命名约定</span><span class="sxs-lookup"><span data-stu-id="51e0f-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="51e0f-118">如果已将媒体库配置为全渠道图像后端，则可使用图像类别指示上传的图像属于哪个类别。</span><span class="sxs-lookup"><span data-stu-id="51e0f-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="51e0f-119">还应遵守一个命名约定以确保其他渠道（如销售点 (POS)）可以正确检索图像。</span><span class="sxs-lookup"><span data-stu-id="51e0f-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="51e0f-120">默认命名约定取决于类别：</span><span class="sxs-lookup"><span data-stu-id="51e0f-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="51e0f-121">目录图像应该命名为 **/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**</span><span class="sxs-lookup"><span data-stu-id="51e0f-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="51e0f-122">类别图像应该命名为 **/Categories/\{CategoryName\}.png**</span><span class="sxs-lookup"><span data-stu-id="51e0f-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="51e0f-123">客户图像应该命名为 **/Customers/\{CustomerNumber\}.jpg**</span><span class="sxs-lookup"><span data-stu-id="51e0f-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="51e0f-124">员工图像应该命名为 **/Workers/\{WorkerNumber\}.jpg**</span><span class="sxs-lookup"><span data-stu-id="51e0f-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="51e0f-125">产品图像应该命名为 **/Products/\{ProductNumber\}_000_001.png**</span><span class="sxs-lookup"><span data-stu-id="51e0f-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="51e0f-126">001 是图像的序号，可以是 001、002、003、004 或 005</span><span class="sxs-lookup"><span data-stu-id="51e0f-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="51e0f-127">产品变型图像应该命名为 **/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**</span><span class="sxs-lookup"><span data-stu-id="51e0f-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="51e0f-128">上传图片</span><span class="sxs-lookup"><span data-stu-id="51e0f-128">Upload an image</span></span>

<span data-ttu-id="51e0f-129">若要在站点构建器中上传图像，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="51e0f-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="51e0f-130">在左侧导航窗格中，选择**媒体库**。</span><span class="sxs-lookup"><span data-stu-id="51e0f-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="51e0f-131">在命令栏上，选择**上传 \> 上传媒体项**。</span><span class="sxs-lookup"><span data-stu-id="51e0f-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="51e0f-132">在文件资源管理器中，浏览到要上传的一个或多个图像文件并选中，然后选择**打开**。</span><span class="sxs-lookup"><span data-stu-id="51e0f-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="51e0f-133">在**上传媒体项**对话框中，输入必需的标题和替代文本。</span><span class="sxs-lookup"><span data-stu-id="51e0f-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="51e0f-134">如果需要，输入可选描述和关键字，然后选择类别。</span><span class="sxs-lookup"><span data-stu-id="51e0f-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="51e0f-135">如果要在上传后立即发布图像，请选中**上传后发布媒体项**复选框。</span><span class="sxs-lookup"><span data-stu-id="51e0f-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="51e0f-136">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="51e0f-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="51e0f-137">上传图像文件夹</span><span class="sxs-lookup"><span data-stu-id="51e0f-137">Upload a folder of images</span></span>

<span data-ttu-id="51e0f-138">若要在站点构建器中上传图像文件夹，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="51e0f-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="51e0f-139">在左侧导航窗格中，选择**媒体库**。</span><span class="sxs-lookup"><span data-stu-id="51e0f-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="51e0f-140">在命令栏上，选择**上传 \> 上传文件夹**。</span><span class="sxs-lookup"><span data-stu-id="51e0f-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="51e0f-141">在文件资源管理器中，浏览到要上传的文件夹并选中，然后选择**打开**。</span><span class="sxs-lookup"><span data-stu-id="51e0f-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="51e0f-142">如果需要，在**上传媒体项**对话框中，输入可选关键字，然后选择类别。</span><span class="sxs-lookup"><span data-stu-id="51e0f-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="51e0f-143">如果要在上传后立即发布文件夹中的图像，请选中**上传后发布媒体项**复选框。</span><span class="sxs-lookup"><span data-stu-id="51e0f-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="51e0f-144">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="51e0f-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51e0f-145">其他资源</span><span class="sxs-lookup"><span data-stu-id="51e0f-145">Additional resources</span></span>

[<span data-ttu-id="51e0f-146">数字资产管理概览</span><span class="sxs-lookup"><span data-stu-id="51e0f-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="51e0f-147">上传视频</span><span class="sxs-lookup"><span data-stu-id="51e0f-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="51e0f-148">上传文件</span><span class="sxs-lookup"><span data-stu-id="51e0f-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="51e0f-149">裁剪图像</span><span class="sxs-lookup"><span data-stu-id="51e0f-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="51e0f-150">自定义图像焦点</span><span class="sxs-lookup"><span data-stu-id="51e0f-150">Customize image focal points</span></span>](dam-custom-focal-point.md)
