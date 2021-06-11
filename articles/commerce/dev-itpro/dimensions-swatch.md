---
title: 将产品维度值配置为作为样本显示
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 总部中将产品维度值配置为样本。
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.openlocfilehash: 08564ce7af7412f2501b917b3496942004402611
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117210"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a><span data-ttu-id="07208-103">将产品维度值配置为作为样本显示</span><span class="sxs-lookup"><span data-stu-id="07208-103">Configure product dimension values to appear as swatches</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="07208-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 总部中将产品维度值配置为样本。</span><span class="sxs-lookup"><span data-stu-id="07208-104">This topic describes how to configure product dimension values as swatches in Microsoft Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="07208-105">有关产品维度的信息，请参阅[产品维度](../../supply-chain/pim/product-dimensions.md)。</span><span class="sxs-lookup"><span data-stu-id="07208-105">For information about product dimensions, see [Product dimensions](../../supply-chain/pim/product-dimensions.md).</span></span>

<span data-ttu-id="07208-106">Dynamics 365 Commerce 支持使用尺寸、样式和颜色维度表示产品变型。</span><span class="sxs-lookup"><span data-stu-id="07208-106">Dynamics 365 Commerce supports the use of size, style, and color dimensions to represent product variants.</span></span> <span data-ttu-id="07208-107">产品维度具有易记名称，此名称显示在产品详细信息页 (PDP) 上，让产品变型可以被选择。</span><span class="sxs-lookup"><span data-stu-id="07208-107">Product dimensions have friendly names that are shown on product details pages (PDPs) so that product variants can be selected.</span></span> <span data-ttu-id="07208-108">这些易记名称的示例包括表示尺寸的“小”、“中”和“大”，以及表示颜色的“黑色”和“棕色”。</span><span class="sxs-lookup"><span data-stu-id="07208-108">Examples of these friendly names include "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="07208-109">但是，如果产品支持很多变体，需要多次选择才能查看每个产品变型的图像。</span><span class="sxs-lookup"><span data-stu-id="07208-109">However, if a product supports many variations, multiple selections are required to view the image for each product variant.</span></span> <span data-ttu-id="07208-110">因此，客户浏览和选择产品变型可能很慢而且繁琐。</span><span class="sxs-lookup"><span data-stu-id="07208-110">Therefore, it can be slow and tedious for customers to browse and select product variants.</span></span>

<span data-ttu-id="07208-111">当维度在 PDP 上显示为样本时，客户可以直观地预览产品的变体。</span><span class="sxs-lookup"><span data-stu-id="07208-111">When dimensions are shown as swatches on PDPs, customers get a visual preview of a product's variations.</span></span> <span data-ttu-id="07208-112">他们可以轻松浏览各种颜色、图案和纹理，并可以快速查看产品变体的不同组合。</span><span class="sxs-lookup"><span data-stu-id="07208-112">They can easily browse a large variety of colors, patterns, and textures, and can quickly view different combinations of product variations.</span></span>

<span data-ttu-id="07208-113">将维度显示为样本这一功能让 Commerce 能够使用十六进制 (hex) 代码和图像将维度显示为样本。</span><span class="sxs-lookup"><span data-stu-id="07208-113">The display dimensions as swatches feature enables Commerce to use hexadecimal (hex) codes and images to show dimensions as swatches.</span></span> <span data-ttu-id="07208-114">而且，相似的维度（如颜色）可以在产品列表页上分组。</span><span class="sxs-lookup"><span data-stu-id="07208-114">In addition, similar dimensions, such as colors, can be grouped on product list pages.</span></span> <span data-ttu-id="07208-115">例如，客户正在搜索蓝色的产品。</span><span class="sxs-lookup"><span data-stu-id="07208-115">For example, a customer is searching for products that are blue.</span></span> <span data-ttu-id="07208-116">如果将各个蓝色维度值分组在一起，搜索结果列表页将显示具有不同蓝色色调的产品。</span><span class="sxs-lookup"><span data-stu-id="07208-116">If the various blue dimension values are grouped together, the search results list page shows products that have the different shades of blue.</span></span> <span data-ttu-id="07208-117">维度分组显著改进了产品提炼体验，通过单个产品搜索查询帮助客户找到更多产品。</span><span class="sxs-lookup"><span data-stu-id="07208-117">Dimension grouping significantly improves the product refinement experience and helps customers find more products through a single product search query.</span></span>

> [!NOTE]
> <span data-ttu-id="07208-118">从 Dynamics 365 Commerce 版本 10.0.20 开始提供将维度显示为样本功能。</span><span class="sxs-lookup"><span data-stu-id="07208-118">The display dimensions as swatches feature is available as of the Dynamics 365 Commerce version 10.0.20 release.</span></span>

<span data-ttu-id="07208-119">下图显示了一个示例，其中颜色在 Commerce PDP 上显示为样本。</span><span class="sxs-lookup"><span data-stu-id="07208-119">The following illustration shows an example where colors appear as swatches on a Commerce PDP.</span></span>

![在产品详细信息页上显示为样本的颜色示例](../dev-itpro/media/swatch_pdp.png)

<span data-ttu-id="07208-121">下图显示了一个示例，其中颜色在 Commerce 搜索结果列表页上显示为样本。</span><span class="sxs-lookup"><span data-stu-id="07208-121">The following illustration shows an example where colors appear as swatches on a Commerce search results list page.</span></span>

![在搜索结果列表页上显示为样本的颜色示例](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a><span data-ttu-id="07208-123">在 Commerce headquarters 中启用将维度显示为样本功能</span><span class="sxs-lookup"><span data-stu-id="07208-123">Enable the display dimensions as swatches feature in Commerce headquarters</span></span>

<span data-ttu-id="07208-124">要在 Commerce headquarters 中启用将维度显示为样本功能，转到 **工作区 \> 功能管理**，打开 **为产品维度值启用图像支持** 功能。</span><span class="sxs-lookup"><span data-stu-id="07208-124">To enable the display dimensions as swatches feature in Commerce headquarters, go to **Workspaces \> Feature management**, and turn on the **Enable image support for product dimension values** feature.</span></span> <span data-ttu-id="07208-125">此功能标志启用后，将在 Commerce headquarters 中的相应表中为每个维度添加三个新字段：**Hexcode**、**URL**（图像）、**RefinerGroup**。</span><span class="sxs-lookup"><span data-stu-id="07208-125">When this feature flag is enabled, three new fields are added for each dimension in the appropriate tables in Commerce headquarters: **Hexcode**, **URL** (for images), and **RefinerGroup**.</span></span>

## <a name="configure-dimension-values-in-commerce-headquarters"></a><span data-ttu-id="07208-126">在 Commerce headquarters 中配置维度值</span><span class="sxs-lookup"><span data-stu-id="07208-126">Configure dimension values in Commerce headquarters</span></span>

<span data-ttu-id="07208-127">尺寸、样式和颜色维度支持将维度显示为样本功能。</span><span class="sxs-lookup"><span data-stu-id="07208-127">The display dimensions as swatches feature is supported for size, style, and color dimensions.</span></span> <span data-ttu-id="07208-128">可以在 Commerce headquarters 中为相应维度指定十六进制代码和图像 URL 值。</span><span class="sxs-lookup"><span data-stu-id="07208-128">Hex code and image URL values for the appropriate dimensions can be specified in Commerce headquarters.</span></span> <span data-ttu-id="07208-129">默认情况下，如果未为维度提供十六进制代码和图像 URL 值，系统将显示维度的易记名称的文本。</span><span class="sxs-lookup"><span data-stu-id="07208-129">By default, if hex code and image URL values aren't provided for a dimension, the system will show the text of the dimension's friendly name.</span></span>

<span data-ttu-id="07208-130">可以在以下任一级别进行配置：</span><span class="sxs-lookup"><span data-stu-id="07208-130">The configuration can be done at any of the following levels:</span></span>

- <span data-ttu-id="07208-131">**维度** – 在 Commerce headquarters 中，通过搜索 **颜色**、**尺寸** 或 **样式** 打开维度的页面。</span><span class="sxs-lookup"><span data-stu-id="07208-131">**Dimension** – In Commerce headquarters, open the page for a dimension by searching for **Color**, **Size**, or **Style**.</span></span> <span data-ttu-id="07208-132">在每个页面上，一个网格将列出维度值。</span><span class="sxs-lookup"><span data-stu-id="07208-132">On each page, a grid lists the dimension values.</span></span> <span data-ttu-id="07208-133">您可以管理显示顺序、十六进制代码和图像 URL 值。</span><span class="sxs-lookup"><span data-stu-id="07208-133">You can manage the display order, hex code, and image URL values.</span></span> <span data-ttu-id="07208-134">下图显示了 **颜色** 页上的示例配置。</span><span class="sxs-lookup"><span data-stu-id="07208-134">The following illustration shows an example configuration on the **Colors** page.</span></span>

    ![“颜色”页上的维度配置的示例](../dev-itpro/media/swatch_Color.PNG)

- <span data-ttu-id="07208-136">**维度组** – 在 Dynamics 365 Commerce 中，您可以使用 **RefinerGroup** 属性创建维度组。</span><span class="sxs-lookup"><span data-stu-id="07208-136">**Dimension group** – In Dynamics 365 Commerce, you can use the **RefinerGroup** property to create dimension groups.</span></span> <span data-ttu-id="07208-137">如果定义了维度组，通过搜索 **颜色组**、**尺寸组** 或 **样式组** 打开相应的页面。</span><span class="sxs-lookup"><span data-stu-id="07208-137">If dimension groups are defined, open the appropriate page by searching for **Color group**, **Size group**, or **Style group**.</span></span> <span data-ttu-id="07208-138">在每个页面上，您可以管理十六进制代码、图像 URL 和提炼组值。</span><span class="sxs-lookup"><span data-stu-id="07208-138">On each page, you can manage hex code, image URL, and refiner group values.</span></span> <span data-ttu-id="07208-139">下图显示了 **颜色组** 页上的示例配置。</span><span class="sxs-lookup"><span data-stu-id="07208-139">The following illustration shows an example configuration on the **Color groups** page.</span></span>

    ![“颜色组”页上的维度配置的示例](../dev-itpro/media/swatch_colorGroup.PNG)

- <span data-ttu-id="07208-141">**产品维度（产品创建期间）** – 创建新产品时，您可以使用 **产品维度** 页输入维度值。</span><span class="sxs-lookup"><span data-stu-id="07208-141">**Product dimension (during product creation)** – When you create a new product, you can use the **Product dimensions** page to enter the dimension values.</span></span> <span data-ttu-id="07208-142">对于现有产品，**Hexcode**、**URL**（图像）和 **RefinerGroup** 字段可能已经设置。</span><span class="sxs-lookup"><span data-stu-id="07208-142">For existing products, the **Hexcode**, **URL** (for images), and **RefinerGroup** fields might already be set.</span></span> <span data-ttu-id="07208-143">不过，您可以根据需要更改这些值。</span><span class="sxs-lookup"><span data-stu-id="07208-143">However, you can change the values as you require.</span></span> <span data-ttu-id="07208-144">下图显示了 **产品维度** 页上的示例配置。</span><span class="sxs-lookup"><span data-stu-id="07208-144">The following illustration shows an example configuration on the **Product dimensions** page.</span></span>

    ![“产品维度”页上的维度配置的示例](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> <span data-ttu-id="07208-146">管理十六进制代码和图像 URL 配置的流程遵照用于管理维度显示顺序的相同模式。</span><span class="sxs-lookup"><span data-stu-id="07208-146">The process of managing hex code and image URL configurations follows the same pattern that is used to manage the display order of dimensions.</span></span>

## <a name="configure-dimension-values-by-using-hex-codes"></a><span data-ttu-id="07208-147">使用十六进制代码配置维度值</span><span class="sxs-lookup"><span data-stu-id="07208-147">Configure dimension values by using hex codes</span></span>

<span data-ttu-id="07208-148">对于大多数颜色维度，应在 Commerce headquarters 中的维度页面上提供十六进制代码颜色值。</span><span class="sxs-lookup"><span data-stu-id="07208-148">For most color dimensions, a hex code color value should be provided on dimension pages in Commerce headquarters.</span></span> <span data-ttu-id="07208-149">例如，黑色应具有十六进制代码值 **#00000**。</span><span class="sxs-lookup"><span data-stu-id="07208-149">For example, the color black should have a hex code value of **#00000**.</span></span> <span data-ttu-id="07208-150">当 Commerce 呈现站点页面时，十六进制代码由彩色样本表示。</span><span class="sxs-lookup"><span data-stu-id="07208-150">When Commerce renders a site page, the hex code is represented by a colored swatch.</span></span>

<span data-ttu-id="07208-151">下图显示了使用十六进制代码值配置颜色维度的示例。</span><span class="sxs-lookup"><span data-stu-id="07208-151">The following illustration shows an example where color dimensions are configured by using hex code values.</span></span>

![使用十六进制代码的维度配置的示例](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a><span data-ttu-id="07208-153">使用图像 URL 配置维度值</span><span class="sxs-lookup"><span data-stu-id="07208-153">Configure dimension values by using image URLs</span></span>

<span data-ttu-id="07208-154">有些颜色维度表示图案，而不是纯色。</span><span class="sxs-lookup"><span data-stu-id="07208-154">Some color dimensions represent patterns, not solid colors.</span></span> <span data-ttu-id="07208-155">例如，某个颜色维度可能被描述为“豹”。</span><span class="sxs-lookup"><span data-stu-id="07208-155">For example, a color dimension might be described as 'leopard.'</span></span> <span data-ttu-id="07208-156">在这些情况下，您可以为样本使用发布的图像而不是十六进制代码来更有效地表示颜色维度。</span><span class="sxs-lookup"><span data-stu-id="07208-156">In these cases, you can more effectively represent the color dimensions by using published images instead of hex codes for swatches.</span></span>

<span data-ttu-id="07208-157">您必须将每个图像上载到 Commerce 站点构建器并进行发布。</span><span class="sxs-lookup"><span data-stu-id="07208-157">You must upload each image to Commerce site builder and publish it.</span></span> <span data-ttu-id="07208-158">然后在 Commerce headquarters 中的相应维度页面上输入发布的图像的图像 URL。</span><span class="sxs-lookup"><span data-stu-id="07208-158">Then enter the image URL for the published image on the appropriate dimension pages in Commerce headquarters.</span></span> <span data-ttu-id="07208-159">如果选择了某个维度要将其显示为样本，但未定义十六进制代码，Commerce 在呈现页面时将进行图像查找。</span><span class="sxs-lookup"><span data-stu-id="07208-159">If a dimension has been selected for display as a swatch, but a hex code isn't defined, Commerce will do an image lookup when it renders the page.</span></span> <span data-ttu-id="07208-160">如果图像查找失败，Commerce 将显示维度的易记名称的文本。</span><span class="sxs-lookup"><span data-stu-id="07208-160">If the image lookup fails, Commerce will show the text of the dimension's friendly name.</span></span>

<span data-ttu-id="07208-161">下图显示了一个示例，其中图像 URL 用于 **颜色** 页上的配置。</span><span class="sxs-lookup"><span data-stu-id="07208-161">The following illustration shows an example where image URLs are used for the configuration on the **Colors** page.</span></span>

![使用图像 URL 的维度配置的示例](../dev-itpro/media/swatch_color_urls.PNG)

<span data-ttu-id="07208-163">您可以使用媒体模板来定义图像 URL，就像为产品和类别图像定义一样。</span><span class="sxs-lookup"><span data-stu-id="07208-163">You can use a media template to define image URLs, just as you can for product and category images.</span></span> <span data-ttu-id="07208-164">当您将图像上载到站点构建器时，文件名约定和文件路径必须一致。</span><span class="sxs-lookup"><span data-stu-id="07208-164">When you upload images to site builder, file name conventions and file paths must be consistent.</span></span>

<span data-ttu-id="07208-165">下图显示了一个示例，其中图像 URL 用于媒体模板的配置。</span><span class="sxs-lookup"><span data-stu-id="07208-165">The following illustration shows an example where image URLs are used for the configuration of a media template.</span></span>

![媒体模板配置示例](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a><span data-ttu-id="07208-167">同时使用十六进制代码和图像 URL 配置维度值</span><span class="sxs-lookup"><span data-stu-id="07208-167">Configure dimension values by using both hex codes and image URLs</span></span>

<span data-ttu-id="07208-168">对于大多数颜色维度，您可以同时配置十六进制代码和图像 URL。</span><span class="sxs-lookup"><span data-stu-id="07208-168">For most color dimensions, you can configure both hex codes and image URLs.</span></span> <span data-ttu-id="07208-169">Commerce 呈现回退逻辑将自动查找十六进制代码或图像 URL 来显示颜色样本。</span><span class="sxs-lookup"><span data-stu-id="07208-169">Commerce rendering fallback logic will automatically look for either a hex code or an image URL to show a color swatch.</span></span> <span data-ttu-id="07208-170">同时使用十六进制代码和图像 URL 配置颜色维度，当颜色数量较多时，可以帮助简化图像管理。</span><span class="sxs-lookup"><span data-stu-id="07208-170">By using both hex codes and image URLs to configure color dimensions, you help simplify image management when the number of colors is large.</span></span>

<span data-ttu-id="07208-171">下图显示了一个示例，其中十六进制代码和图像 URL 同时用于 **颜色** 页上的配置。</span><span class="sxs-lookup"><span data-stu-id="07208-171">The following illustration shows an example where both hex codes and image URLs are used for the configuration on the **Colors** page.</span></span>

![同时使用十六进制代码和图像 URL 的维度配置的示例](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a><span data-ttu-id="07208-173">配置提炼组</span><span class="sxs-lookup"><span data-stu-id="07208-173">Configure refiner groups</span></span>

<span data-ttu-id="07208-174">当您为维度值定义十六进制代码或图像 URL 时，您还可以为 **RefinerGroup** 字段指定值。</span><span class="sxs-lookup"><span data-stu-id="07208-174">When you define a hex code or image URL for a dimension value, you can also specify a value for the **RefinerGroup** field.</span></span> <span data-ttu-id="07208-175">此字段定义应在提炼体验中用于对相似维度值进行分组的维度。</span><span class="sxs-lookup"><span data-stu-id="07208-175">This field defines the dimension that should be used to group similar dimension values in the refiner experience.</span></span>

<span data-ttu-id="07208-176">例如，如果您的颜色维度值是“蓝色”、“蓝色格子”、“涂蓝色”和“深蓝色”，每个值都映射到不同的十六进制代码或图像 URL。</span><span class="sxs-lookup"><span data-stu-id="07208-176">For example, if your color dimension values are "blue," "blue plaid," "blue wash," and "dark blue," each value is mapped to a different hex code or image URL.</span></span> <span data-ttu-id="07208-177">因此，每个值都将在相应产品的 PDP 和产品卡上显示为不同的颜色。</span><span class="sxs-lookup"><span data-stu-id="07208-177">Therefore, each value will appear as a different color on PDPs and product cards for the appropriate products.</span></span> <span data-ttu-id="07208-178">但是，如果您将所有这些颜色维度值映射到 **蓝色** 的 **RefinerGroup** 值，搜索“蓝色”产品将生成具有“蓝色”、“蓝格子”、“涂蓝色”和“深蓝色”维度颜色值的产品的列表页搜索结果。</span><span class="sxs-lookup"><span data-stu-id="07208-178">However, if you map all those color dimension values to a **RefinerGroup** value of **Blue**, a search for "blue" products will generate list page search results for products that have dimension color values of "blue," "blue plaid," "blue wash," and "dark blue".</span></span>

<span data-ttu-id="07208-179">下图中的示例显示了 Commerce headquarters 中 **颜色** 和 **RefinerGroup** 属性之间的关系。</span><span class="sxs-lookup"><span data-stu-id="07208-179">The example in the following illustration shows the relationship between the **Color** and **RefinerGroup** properties in Commerce headquarters.</span></span>

![提炼组管理示例](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a><span data-ttu-id="07208-181">在 Commerce 站点构建器中管理图像</span><span class="sxs-lookup"><span data-stu-id="07208-181">Manage images in Commerce site builder</span></span>

<span data-ttu-id="07208-182">如果将图像 URL 用于任何维度值，则必须将相应的图像上载到 Commerce 站点构建器。</span><span class="sxs-lookup"><span data-stu-id="07208-182">If image URLs are used for any dimension values, the corresponding images must be uploaded to Commerce site builder.</span></span> <span data-ttu-id="07208-183">每个图像的位置应与在 Commerce headquarters 中为该图像定义的文件名和文件夹路径匹配。</span><span class="sxs-lookup"><span data-stu-id="07208-183">The location of each image should match the file name and folder path that are defined for the image in Commerce headquarters.</span></span> <span data-ttu-id="07208-184">图像文件必须上载到站点构建器中的相应类别位置。</span><span class="sxs-lookup"><span data-stu-id="07208-184">Image files must be uploaded to the appropriate category locations in site builder.</span></span> <span data-ttu-id="07208-185">例如，颜色图像必须上载到 **颜色** 类别文件夹。</span><span class="sxs-lookup"><span data-stu-id="07208-185">For example, color images must be uploaded to the **Color** category folder.</span></span> <span data-ttu-id="07208-186">有关如何将图像上载到站点构建器的详细信息，请参阅[上载图像](../dam-upload-images.md)。</span><span class="sxs-lookup"><span data-stu-id="07208-186">For more information about how to upload images to site builder, see [Upload images](../dam-upload-images.md).</span></span>

<span data-ttu-id="07208-187">下图显示了一个示例，其中 **上载文件** 对话框用于将图像上载到站点构建器媒体库。</span><span class="sxs-lookup"><span data-stu-id="07208-187">The following illustration shows an example where the **Upload files** dialog box is being used to upload images to the site builder media library.</span></span> <span data-ttu-id="07208-188">可供选择的 **尺寸**、**颜色** 和 **样式** 类别突出显示。</span><span class="sxs-lookup"><span data-stu-id="07208-188">It highlights the **Size**, **Color**, and **Style** categories that are available for selection.</span></span>

![上载到站点构建器媒体库期间的图像文件类别的示例](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a><span data-ttu-id="07208-190">在电子商务站点页面上启用样本显示</span><span class="sxs-lookup"><span data-stu-id="07208-190">Enable swatch display on e-commerce site pages</span></span>

<span data-ttu-id="07208-191">您必须在 Commerce headquarters 中配置维度站点设置，然后样本才能够显示在需要选择维度的电子商务站点页面（如 PDP 和列表页）上。</span><span class="sxs-lookup"><span data-stu-id="07208-191">Before swatches can appear on e-commerce site pages that require dimension selection, such as PDPs and list pages, you must configure dimension site settings in Commerce headquarters.</span></span> <span data-ttu-id="07208-192">有关详细信息，请参阅[应用维度的站点设置](../dimension-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="07208-192">For more information, see [Apply site settings for dimensions](../dimension-settings.md).</span></span>

<span data-ttu-id="07208-193">此外，您应该为搜索结果模块启用 **在搜索结果中包括产品属性** 属性。</span><span class="sxs-lookup"><span data-stu-id="07208-193">In addition, you should enable the **Include product attributes in search results** property for search results modules.</span></span> <span data-ttu-id="07208-194">如果您的站点使用自定义类别页面，您应该更新在这些页面上使用的搜索结果模块，以启用 **在搜索结果中包括产品属性** 属性。</span><span class="sxs-lookup"><span data-stu-id="07208-194">If your site uses customized category pages, you should update the search results modules that are used on those pages, so that the **Include product attributes in search results** property is enabled.</span></span> <span data-ttu-id="07208-195">有关详细信息，请参阅[搜索结果模块](../search-result-module.md)。</span><span class="sxs-lookup"><span data-stu-id="07208-195">For more information, see [Search results module](../search-result-module.md).</span></span>

## <a name="display-swatches-in-pos-and-other-channels"></a><span data-ttu-id="07208-196">在 POS 和其他渠道中显示样本</span><span class="sxs-lookup"><span data-stu-id="07208-196">Display swatches in POS and other channels</span></span>

<span data-ttu-id="07208-197">Commerce 目前没有支持在销售点 (POS) 和其他渠道中显示样本的现成实现。</span><span class="sxs-lookup"><span data-stu-id="07208-197">Commerce doesn't currently have an out-of-box implementation that supports the display of swatches in Point of Sale (POS) and other channels.</span></span> <span data-ttu-id="07208-198">不过，您可以将样本显示功能作为扩展来实现，使渠道 API 返回呈现样本所需的十六进制代码和图像 URL。</span><span class="sxs-lookup"><span data-stu-id="07208-198">However, you can implement swatch display functionality as an extension that makes channel APIs return the hex codes and image URLs that are required to render swatches.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07208-199">其他资源</span><span class="sxs-lookup"><span data-stu-id="07208-199">Additional resources</span></span>

[<span data-ttu-id="07208-200">搜索结果模块</span><span class="sxs-lookup"><span data-stu-id="07208-200">Search results module</span></span>](../search-result-module.md)

[<span data-ttu-id="07208-201">应用维度的站点设置</span><span class="sxs-lookup"><span data-stu-id="07208-201">Apply site settings for dimensions</span></span>](../dimension-settings.md)

[<span data-ttu-id="07208-202">产品维度</span><span class="sxs-lookup"><span data-stu-id="07208-202">Product dimensions</span></span>](../../supply-chain/pim/product-dimensions.md)

[<span data-ttu-id="07208-203">上传图像</span><span class="sxs-lookup"><span data-stu-id="07208-203">Upload image</span></span>](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
