---
title: 媒体库模块
description: 此主题介绍媒体库模块以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b0b1ec7324ff60ee7cdd01c97c8c08260bd8c947
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802807"
---
# <a name="media-gallery-module"></a><span data-ttu-id="887a3-103">媒体库模块</span><span class="sxs-lookup"><span data-stu-id="887a3-103">Media gallery module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="887a3-104">此主题介绍媒体库模块以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="887a3-104">This topic covers media gallery modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="887a3-105">媒体库模块在库视图中显示一个或多个图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-105">Media gallery modules show one or more images in a gallery view.</span></span> <span data-ttu-id="887a3-106">媒体库模块支持缩略图，其可以水平排列（作为图像下的一行），或垂直排列（作为图像旁边的一列）。</span><span class="sxs-lookup"><span data-stu-id="887a3-106">Media gallery modules support thumbnail images, which can be arranged either horizontally (as a row below the image) or vertically (as a column next to the image).</span></span> <span data-ttu-id="887a3-107">媒体库模块还提供了使图像能够缩放（放大）或以全屏模式查看的功能。</span><span class="sxs-lookup"><span data-stu-id="887a3-107">Media gallery modules also provide capabilities that enable images to be zoomed (magnified) or viewed in full-screen mode.</span></span> <span data-ttu-id="887a3-108">要在媒体库模块中呈现，图像必须在 Commerce 站点构建器“媒体库”中可用。</span><span class="sxs-lookup"><span data-stu-id="887a3-108">To be rendered in a media gallery module, an image must be available in the Commerce site builder Media Library.</span></span> <span data-ttu-id="887a3-109">当前，媒体库模块仅支持图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-109">Currently, media gallery modules support only images.</span></span>

<span data-ttu-id="887a3-110">在默认模式下，媒体库模块使用产品详细信息页面 (PDP) 的页面上下文中提供的产品 ID 呈现相应的产品图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-110">In the default mode, a media gallery module uses the product ID that is available from the page context of a product details page (PDP) to render the corresponding product images.</span></span> <span data-ttu-id="887a3-111">在 Commerce Headquarters 中，必须为所有产品定义媒体文件路径。</span><span class="sxs-lookup"><span data-stu-id="887a3-111">In Commerce headquarters, a media file path must be defined for all products.</span></span> <span data-ttu-id="887a3-112">然后应根据在 Commerce Headquarters 中为产品定义的文件路径，将图像上载到站点构建器媒体库中。</span><span class="sxs-lookup"><span data-stu-id="887a3-112">Images should then be uploaded to the site builder Media Library according to the file path that was defined for the products in Commerce headquarters.</span></span> <span data-ttu-id="887a3-113">这些图像包括产品和任意产品变型的图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-113">These images include images for products and any product variants.</span></span> <span data-ttu-id="887a3-114">有关如何将图像上载到站点构建器媒体库的详细信息，请参阅[上载图像](dam-upload-images.md)。</span><span class="sxs-lookup"><span data-stu-id="887a3-114">For more information about how to upload images to site builder Media Library, see [Upload images](dam-upload-images.md).</span></span>

<span data-ttu-id="887a3-115">或者，媒体库模块可以在图像库页面上托管一组完全经过挑选的图像，其中没有对产品 ID 或页面上下文的依赖关系。</span><span class="sxs-lookup"><span data-stu-id="887a3-115">Alternatively, a media gallery module can host a fully curated set of images on an image gallery page, where there are no dependencies on the product ID or page context.</span></span> <span data-ttu-id="887a3-116">在这种情况下，必须将图像上载到站点构建器媒体库并在站点构建器中指定图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-116">In this case, images must be uploaded to site builder Media Library and specified in site builder.</span></span>

<span data-ttu-id="887a3-117">以下是媒体库模块的一些使用示例：</span><span class="sxs-lookup"><span data-stu-id="887a3-117">Here are some usage examples for media gallery modules:</span></span>

- <span data-ttu-id="887a3-118">在 PDP 上呈现产品图像</span><span class="sxs-lookup"><span data-stu-id="887a3-118">Rendering product images on a PDP</span></span>
- <span data-ttu-id="887a3-119">在产品市场营销页面上呈现产品图像</span><span class="sxs-lookup"><span data-stu-id="887a3-119">Rendering product images on a product marketing page</span></span>
- <span data-ttu-id="887a3-120">在市场营销页面（如库页面）上展示一组精选的图像</span><span class="sxs-lookup"><span data-stu-id="887a3-120">Showcasing a curated set of images on a marketing page, such as a gallery page</span></span>

<span data-ttu-id="887a3-121">在下图的示例中，PDP 上的购买框使用媒体库模块托管产品图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-121">In the example in the following illustration, a buy box on a PDP hosts product images by using a media gallery module.</span></span>

![使用媒体库模块托管产品图像的产品详细信息页面上的购买框示例](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a><span data-ttu-id="887a3-123">媒体库属性</span><span class="sxs-lookup"><span data-stu-id="887a3-123">Media gallery properties</span></span>

| <span data-ttu-id="887a3-124">属性名称</span><span class="sxs-lookup"><span data-stu-id="887a3-124">Property name</span></span> | <span data-ttu-id="887a3-125">值</span><span class="sxs-lookup"><span data-stu-id="887a3-125">Values</span></span> | <span data-ttu-id="887a3-126">说明</span><span class="sxs-lookup"><span data-stu-id="887a3-126">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="887a3-127">图像源</span><span class="sxs-lookup"><span data-stu-id="887a3-127">Image source</span></span> | <span data-ttu-id="887a3-128">**页面上下文** 或 **产品 ID**</span><span class="sxs-lookup"><span data-stu-id="887a3-128">**Page context** or **Product ID**</span></span> | <span data-ttu-id="887a3-129">默认值为 **页面上下文**。</span><span class="sxs-lookup"><span data-stu-id="887a3-129">The default value is **Page context**.</span></span> <span data-ttu-id="887a3-130">如果选择 **页面上下文**，模块将预期页面会提供产品 ID 信息。</span><span class="sxs-lookup"><span data-stu-id="887a3-130">If **Page context** is selected, the module expects the page to provide the product ID information.</span></span> <span data-ttu-id="887a3-131">如果选择了 **产品 ID**，必须提供图像的产品 ID 作为 **产品 ID** 属性的值。</span><span class="sxs-lookup"><span data-stu-id="887a3-131">If **Product ID** is selected, the product ID for an image must be provided as the value of the **Product ID** property.</span></span> <span data-ttu-id="887a3-132">Commerce 版本 10.0.12 中提供了此功能。</span><span class="sxs-lookup"><span data-stu-id="887a3-132">This capability is available in Commerce version 10.0.12.</span></span> |
| <span data-ttu-id="887a3-133">产品 ID</span><span class="sxs-lookup"><span data-stu-id="887a3-133">Product ID</span></span> | <span data-ttu-id="887a3-134">产品 ID</span><span class="sxs-lookup"><span data-stu-id="887a3-134">A product ID</span></span> | <span data-ttu-id="887a3-135">仅当 **图片源** 属性的值为 **产品 ID** 时，此属性才适用。</span><span class="sxs-lookup"><span data-stu-id="887a3-135">This property is applicable only if the value of the **Image source** property is **Product ID**.</span></span> |
| <span data-ttu-id="887a3-136">图像缩放</span><span class="sxs-lookup"><span data-stu-id="887a3-136">Image zoom</span></span> | <span data-ttu-id="887a3-137">**内联** 或 **容器**</span><span class="sxs-lookup"><span data-stu-id="887a3-137">**Inline** or **Container**</span></span> | <span data-ttu-id="887a3-138">此属性使用户可以在媒体库模块中缩放图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-138">This property lets the user zoom images in the media gallery module.</span></span> <span data-ttu-id="887a3-139">可以内联缩放图像，也可以在图像旁边的单独容器中缩放图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-139">An image can be zoomed either inline or in a separate container next to the image.</span></span> <span data-ttu-id="887a3-140">此功能在 10.0.12 中提供</span><span class="sxs-lookup"><span data-stu-id="887a3-140">This capability is available in 10.0.12</span></span> |
| <span data-ttu-id="887a3-141">缩放比例</span><span class="sxs-lookup"><span data-stu-id="887a3-141">Zoom scale</span></span> | <span data-ttu-id="887a3-142">小数</span><span class="sxs-lookup"><span data-stu-id="887a3-142">A decimal number</span></span> | <span data-ttu-id="887a3-143">此属性指定缩放图像的比例系数。</span><span class="sxs-lookup"><span data-stu-id="887a3-143">This property specifies the scale factor for zooming images.</span></span> <span data-ttu-id="887a3-144">例如，如果值设置为 **2.5**，图像将放大 2.5 倍。</span><span class="sxs-lookup"><span data-stu-id="887a3-144">For example, if the value is set to **2.5**, images are magnified 2.5 times.</span></span>|
| <span data-ttu-id="887a3-145">全屏</span><span class="sxs-lookup"><span data-stu-id="887a3-145">Full screen</span></span> | <span data-ttu-id="887a3-146">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="887a3-146">**True** or **False**</span></span> | <span data-ttu-id="887a3-147">此属性指定是否可以在全屏模式下查看图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-147">This property specifies whether images can be viewed in full-screen mode.</span></span> <span data-ttu-id="887a3-148">在全屏模式下，如果打开了缩放功能，也可以进一步放大图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-148">In full-screen mode, images can be also be further magnified if the zoom capability is turned on.</span></span> <span data-ttu-id="887a3-149">Commerce 版本 10.0.13 中提供了此功能。</span><span class="sxs-lookup"><span data-stu-id="887a3-149">This capability is available in Commerce version 10.0.13.</span></span> |
| <span data-ttu-id="887a3-150">图像</span><span class="sxs-lookup"><span data-stu-id="887a3-150">Images</span></span> | <span data-ttu-id="887a3-151">从站点构建器媒体库中选择的图像</span><span class="sxs-lookup"><span data-stu-id="887a3-151">Images that are selected from site builder Media Library</span></span> | <span data-ttu-id="887a3-152">除了从产品呈现外，还可以为媒体库模块挑选图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-152">In addition to being rendered from a product, images can be curated for a media gallery module.</span></span> <span data-ttu-id="887a3-153">这些图像将被附加到任何可用的产品图像上。</span><span class="sxs-lookup"><span data-stu-id="887a3-153">These images will be appended to any product images that are available.</span></span> <span data-ttu-id="887a3-154">Commerce 版本 10.0.12 中提供了此功能。</span><span class="sxs-lookup"><span data-stu-id="887a3-154">This capability is available in Commerce version 10.0.12.</span></span> |
| <span data-ttu-id="887a3-155">缩略图方向</span><span class="sxs-lookup"><span data-stu-id="887a3-155">Thumbnail orientation</span></span> | <span data-ttu-id="887a3-156">**垂直** 或 **水平**</span><span class="sxs-lookup"><span data-stu-id="887a3-156">**Vertical** or **Horizontal**</span></span> | <span data-ttu-id="887a3-157">此属性指定缩略图图像应显示为垂直条还是水平条。</span><span class="sxs-lookup"><span data-stu-id="887a3-157">This property specifies whether thumbnail images should be shown in a vertical strip or a horizontal strip.</span></span> |

<span data-ttu-id="887a3-158">下图显示了一个媒体库模块的示例，其中全屏和缩放选项可用。</span><span class="sxs-lookup"><span data-stu-id="887a3-158">The following illustration shows an example of a media gallery module where the full-screen and zoom options are available.</span></span>

![全屏和缩放选项可用的媒体库模块的示例](./media/ecommerce-media-zoom.png)

<span data-ttu-id="887a3-160">下图显示了具有精选图像的媒体库模块的示例（即，指定图像不依赖于产品 ID 或页面上下文）。</span><span class="sxs-lookup"><span data-stu-id="887a3-160">The following illustration shows an example of a media gallery module that has curated images (that is, the specified images aren't dependent on the product ID or page context).</span></span>

![具有精选图像的媒体库模块的示例](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="887a3-162">Commerce Scale Unit 交互</span><span class="sxs-lookup"><span data-stu-id="887a3-162">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="887a3-163">从页面上下文派生图像源时，将使用 PDP 中的产品 ID 检索图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-163">When the image source is derived from the page context, the product ID from the PDP is used to retrieve the images.</span></span> <span data-ttu-id="887a3-164">媒体库模块使用 Commerce Scale Unit 应用程序编程接口 (API) 检索产品的图像文件路径。</span><span class="sxs-lookup"><span data-stu-id="887a3-164">The media gallery module retrieves the image file path for products by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="887a3-165">然后从媒体库中提取图像，以可以在模块中呈现。</span><span class="sxs-lookup"><span data-stu-id="887a3-165">The images are then pulled from the Media Library so that they can be rendered in the module.</span></span>

## <a name="add-a-media-gallery-module-to-a-page"></a><span data-ttu-id="887a3-166">向页面添加媒体库模块</span><span class="sxs-lookup"><span data-stu-id="887a3-166">Add a media gallery module to a page</span></span>

<span data-ttu-id="887a3-167">若要向市场营销页面添加媒体库模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="887a3-167">To add a media gallery module to a marketing page, follow these steps.</span></span>

1. <span data-ttu-id="887a3-168">转到 **模板**，选择 **新建** 创建新模板。</span><span class="sxs-lookup"><span data-stu-id="887a3-168">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="887a3-169">在 **新建模板** 对话框的 **模板名称** 下，输入 **市场营销模板**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="887a3-169">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="887a3-170">在 **正文** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="887a3-170">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="887a3-171">在 **添加模块** 对话框中，选择 **默认页面** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="887a3-171">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="887a3-172">在默认页的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="887a3-172">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="887a3-173">在 **添加模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="887a3-173">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="887a3-174">选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="887a3-174">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="887a3-175">转到 **页面**，选择 **新建** 创建新页面。</span><span class="sxs-lookup"><span data-stu-id="887a3-175">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="887a3-176">在 **选择模板** 对话框中，选择 **市场营销模板** 模板。</span><span class="sxs-lookup"><span data-stu-id="887a3-176">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="887a3-177">在 **页面名称** 下，输入 **媒体库页面**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="887a3-177">Under **Page name**, enter **Media gallery page**, and then select **OK**.</span></span>
1. <span data-ttu-id="887a3-178">在新页面的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="887a3-178">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="887a3-179">在 **添加模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="887a3-179">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="887a3-180">在 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="887a3-180">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="887a3-181">在 **添加模块** 对话框中，选择 **媒体库** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="887a3-181">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="887a3-182">在媒体库模块的属性窗格中，在 **图像源** 下，选择 **Productid**。</span><span class="sxs-lookup"><span data-stu-id="887a3-182">In the property pane for the media gallery module, under **Image source**, select **Productid**.</span></span> <span data-ttu-id="887a3-183">然后，在 **产品 ID** 字段中，输入产品 ID。</span><span class="sxs-lookup"><span data-stu-id="887a3-183">Then, in the **Product id** field, enter a product ID.</span></span>
1. <span data-ttu-id="887a3-184">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="887a3-184">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="887a3-185">您应该能够在库视图中看到产品的图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-185">You should be able to see the images for the product in a gallery view.</span></span>
1. <span data-ttu-id="887a3-186">要仅使用精选图像，在属性窗格中的 **图像源** 下，选择 **Productid**。</span><span class="sxs-lookup"><span data-stu-id="887a3-186">To use only curated images, in the property pane, under **Image source**, select **Productid**.</span></span> <span data-ttu-id="887a3-187">然后，在 **图像** 下，按需多次选择 **添加图像** 来从媒体库添加图像。</span><span class="sxs-lookup"><span data-stu-id="887a3-187">Then, under **Images**, select **Add an image** as many times as required to add images from the Media Library.</span></span>
1. <span data-ttu-id="887a3-188">设置您想要设置的任何其他属性，如 **图像缩放**、**缩放系数** 和 **缩略图方向**。</span><span class="sxs-lookup"><span data-stu-id="887a3-188">Set any additional properties that you want to set, such as **Image zoom**, **Zoom factor**, and **Thumbnails orientation**.</span></span>
1. <span data-ttu-id="887a3-189">完成后，选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="887a3-189">When you've finished, select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="887a3-190">其他资源</span><span class="sxs-lookup"><span data-stu-id="887a3-190">Additional resources</span></span>

[<span data-ttu-id="887a3-191">模块库概述</span><span class="sxs-lookup"><span data-stu-id="887a3-191">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="887a3-192">购买框模块</span><span class="sxs-lookup"><span data-stu-id="887a3-192">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="887a3-193">容器模块</span><span class="sxs-lookup"><span data-stu-id="887a3-193">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="887a3-194">上传图像</span><span class="sxs-lookup"><span data-stu-id="887a3-194">Upload images</span></span>](dam-upload-images.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]