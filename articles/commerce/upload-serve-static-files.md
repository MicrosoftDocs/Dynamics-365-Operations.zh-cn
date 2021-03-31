---
title: 上传并处理静态文件
description: 此主题介绍如何将静态文件上传到 Microsoft Dynamics 365 Commerce 站点构建器，以及如何创建可用于请求该文件的自定义 URL 和文件名。
author: StuHarg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: aba9dde2ed9d5fa09e92fcdd784a53f208930eda
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211011"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="2d4e7-103">上传并处理静态文件</span><span class="sxs-lookup"><span data-stu-id="2d4e7-103">Upload and serve static files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2d4e7-104">此主题介绍如何将静态文件上传到 Microsoft Dynamics 365 Commerce 站点构建器，以及如何创建可用于请求该文件的自定义 URL 和文件名。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="2d4e7-105">有些第三方连接器需要文件从电子商务站点托管和提供。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="2d4e7-106">这些连接器预期文件将由对特定回叫 URL 路径和文件名的请求返回。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="2d4e7-107">因此，此主题说明如何在 Dynamics 365 Commerce 电子商务站点上载和提供具有用户可定义 URL 和文件名的静态文件。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="2d4e7-108">创建返回静态文件的站点 URL</span><span class="sxs-lookup"><span data-stu-id="2d4e7-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="2d4e7-109">若要在 Commerce 站点构建器中创建返回静态文件的站点 URL，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2d4e7-110">转到您的站点的媒体库，上载应由对您定义的 URL 的请求提供的文件。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="2d4e7-111">如果您已经上载文件，则可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="2d4e7-112">转到您的站点的 **URL**。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="2d4e7-113">选择 **新建 \> 新建 URL**。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="2d4e7-114">在 **新建 URL** 对话框中，选择 **媒体库资产**。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="2d4e7-115">在 **URL 路径** 字段中，输入 URL 路径。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="2d4e7-116">在路径中包括文件名。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="2d4e7-117">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-117">Select **Next**.</span></span> <span data-ttu-id="2d4e7-118">媒体库将打开，显示所有已上载的 **文档** 类型的媒体资产。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="2d4e7-119">选择应为对您在步骤 5 中定义的 URL 的请求提供的文件。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="2d4e7-120">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-120">Select **Save**.</span></span>

<span data-ttu-id="2d4e7-121">此时，您创建的 URL 处于草稿状态。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="2d4e7-122">在您发布 URL 之前，URL 指向的文件不会返回。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="2d4e7-123">在发布 URL 之前，您可以验证它是否返回正确的数据。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="2d4e7-124">验证和发布 URL</span><span class="sxs-lookup"><span data-stu-id="2d4e7-124">Validate and publish a URL</span></span>

<span data-ttu-id="2d4e7-125">要在发布之前验证 URL，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="2d4e7-126">转到您的站点的 **URL**，选择要预览的 URL。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="2d4e7-127">在右侧的属性窗格中，在 **编辑** 按钮下，选择正确的 URL 链接。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="2d4e7-128">一个新浏览器窗口将打开，您应会收到 404 错误。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="2d4e7-129">将 **?preview=inprogress** 查询字符串追加到 URL（例如，`https://yoursite.com/callback.html?preview=inprogress`），然后重新加载页面。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="2d4e7-130">您上载到媒体库的文件应在响应中返回。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="2d4e7-131">验证 URL 后，可以将其发布。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="2d4e7-132">转到您的站点的 **URL**，选择 URL。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="2d4e7-133">在命令栏上选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="2d4e7-134">更新 URL 指向的文件</span><span class="sxs-lookup"><span data-stu-id="2d4e7-134">Update the file that a URL points to</span></span>

<span data-ttu-id="2d4e7-135">URL 发布后，您可以对它进行更新，让它指向另一个文件。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="2d4e7-136">或者，您可以更新 URL，让它指向不同的资源类型，如下一节中所述。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="2d4e7-137">例如，您可以将 URL 指向内部页面或重定向。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="2d4e7-138">要更新 URL 指向的文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="2d4e7-139">转到您的站点的 **URL**，选择要更新的 URL。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="2d4e7-140">在右侧的属性窗格中，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="2d4e7-141">在 **URL 分配** 下，选择 **步骤 2** 框，然后从媒体库中选择一个新文档。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="2d4e7-142">选择 **应用**。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="2d4e7-143">更新 URL 指向的资产类型</span><span class="sxs-lookup"><span data-stu-id="2d4e7-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="2d4e7-144">您还可以更新 URL，让它指向其他类型的资产（资源），如内部页面或重定向。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="2d4e7-145">要更新 URL 指向的资产类型，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="2d4e7-146">转到您的站点的 **URL**，选择要更新的 URL。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="2d4e7-147">在右侧的属性窗格中，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="2d4e7-148">在 **URL 分配** 下，在 **步骤 1** 下，选择其他资产类型。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="2d4e7-149">选择 **步骤 2** 框，然后选择新资产。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="2d4e7-150">选择 **应用**。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="2d4e7-151">更改 URL 路径</span><span class="sxs-lookup"><span data-stu-id="2d4e7-151">Change the URL path</span></span>

<span data-ttu-id="2d4e7-152">创建 URL 后，它的路径无法更改。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="2d4e7-153">如果必须更改用于提供文件或任何其他类型资源的 URL 路径，必须创建一个新 URL，将其映射到现有文件或其他资源，然后取消发布并删除旧 URL。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="2d4e7-154">若要更改 URL 路径，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="2d4e7-155">要创建新的 URL 并将其映射到现有文件或另一个资源，请按照此主题前面的[创建返回静态文件的站点 URL](#create-a-site-url-that-returns-a-static-file) 一节中的说明操作。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="2d4e7-156">选择新 URL，然后在命令栏上选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="2d4e7-157">新 URL 将发布。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-157">The new URL is published.</span></span>
1. <span data-ttu-id="2d4e7-158">要取消发布旧 URL，选择它，然后在命令栏上选择 **取消发布**。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="2d4e7-159">现在，您可以根据需要删除旧 URL 了。</span><span class="sxs-lookup"><span data-stu-id="2d4e7-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d4e7-160">其他资源</span><span class="sxs-lookup"><span data-stu-id="2d4e7-160">Additional resources</span></span>

[<span data-ttu-id="2d4e7-161">数字资产管理概览</span><span class="sxs-lookup"><span data-stu-id="2d4e7-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="2d4e7-162">上传图像</span><span class="sxs-lookup"><span data-stu-id="2d4e7-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="2d4e7-163">上传视频</span><span class="sxs-lookup"><span data-stu-id="2d4e7-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="2d4e7-164">上传图像和视频以外的文件</span><span class="sxs-lookup"><span data-stu-id="2d4e7-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="2d4e7-165">裁剪图像</span><span class="sxs-lookup"><span data-stu-id="2d4e7-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="2d4e7-166">自定义图像焦点</span><span class="sxs-lookup"><span data-stu-id="2d4e7-166">Customize image focal points</span></span>](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]