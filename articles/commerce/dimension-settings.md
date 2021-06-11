---
title: 应用产品维度的显示设置
description: 本主题介绍产品维度的显示设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117211"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="6ede4-103">应用产品维度的显示设置</span><span class="sxs-lookup"><span data-stu-id="6ede4-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="6ede4-104">本主题介绍产品维度的显示设置，并介绍如何在 Microsoft Dynamics 365 Commerce 中应用这些设置。</span><span class="sxs-lookup"><span data-stu-id="6ede4-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6ede4-105">Dynamics 365 Commerce 支持使用尺寸、样式和颜色维度来区分产品变型。</span><span class="sxs-lookup"><span data-stu-id="6ede4-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="6ede4-106">维度通常显示为文本值，如“小”、“中”和“大”是尺寸，“黑色”和“棕色”是颜色。</span><span class="sxs-lookup"><span data-stu-id="6ede4-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="6ede4-107">但是，如果产品支持很多变体，浏览产品变型可能很难，因为需要多次选择才能查看每个变型的图像。</span><span class="sxs-lookup"><span data-stu-id="6ede4-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="6ede4-108">为了使浏览产品变型更加容易，Commerce 的 10.0.20 版本可以使用图像和十六进制 (hex) 代码将维度显示为样本。</span><span class="sxs-lookup"><span data-stu-id="6ede4-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="6ede4-109">在 Commerce 站点构建器中，维度设置在 **站点设置 \> 扩展 \> 维度设置** 处定义。</span><span class="sxs-lookup"><span data-stu-id="6ede4-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="6ede4-110">下图显示了站点构建器中维度设置的示例。</span><span class="sxs-lookup"><span data-stu-id="6ede4-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Commerce 站点构建器中站点设置的示例](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="6ede4-112">有两个维度设置可用：</span><span class="sxs-lookup"><span data-stu-id="6ede4-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="6ede4-113">**显示为图像的维度** – 指定应在电子商务站点页面（如产品详细信息页面 (PDP) 和搜索结果列表页面）上显示为样本的维度。</span><span class="sxs-lookup"><span data-stu-id="6ede4-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="6ede4-114">颜色、尺寸和样式维度的任何组合都可以显示为一个样本。</span><span class="sxs-lookup"><span data-stu-id="6ede4-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="6ede4-115">如果选择了一个维度要将其显示为样本，Commerce 模块呈现将查找可用的十六进制代码样本配置。</span><span class="sxs-lookup"><span data-stu-id="6ede4-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="6ede4-116">如果未配置十六进制代码，系统逻辑将查找图像 URL 样本的配置。</span><span class="sxs-lookup"><span data-stu-id="6ede4-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="6ede4-117">如果既未配置十六进制代码，也未配置图像 URL，将显示文本。</span><span class="sxs-lookup"><span data-stu-id="6ede4-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="6ede4-118">下图显示了一个示例，其中电子商务站点上的 PDP 包含颜色和尺寸样本。</span><span class="sxs-lookup"><span data-stu-id="6ede4-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="6ede4-119">在此示例中，为颜色维度配置了十六进制代码。</span><span class="sxs-lookup"><span data-stu-id="6ede4-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="6ede4-120">因此，样本显示为颜色。</span><span class="sxs-lookup"><span data-stu-id="6ede4-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="6ede4-121">但是，没有为尺寸维度配置十六进制代码和图像 URL。</span><span class="sxs-lookup"><span data-stu-id="6ede4-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="6ede4-122">因此，显示文本。</span><span class="sxs-lookup"><span data-stu-id="6ede4-122">Therefore, text is shown.</span></span>

    ![在电子商务产品详细信息页上显示为样本的颜色维度的示例](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="6ede4-124">**在产品卡中显示的维度** – 指定应在列表和列表页上显示的产品卡上显示哪些维度。</span><span class="sxs-lookup"><span data-stu-id="6ede4-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="6ede4-125">必须为维度启用此设置，维度才能够显示在产品卡上。</span><span class="sxs-lookup"><span data-stu-id="6ede4-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="6ede4-126">**显示为图像的维度** 设置也应启用。</span><span class="sxs-lookup"><span data-stu-id="6ede4-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="6ede4-127">产品卡上的样本选择行为针对颜色维度进行了优化。</span><span class="sxs-lookup"><span data-stu-id="6ede4-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="6ede4-128">对于其他维度，可能需要扩展视图来自定义样本选择行为。</span><span class="sxs-lookup"><span data-stu-id="6ede4-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="6ede4-129">下图显示了一个示例，其中电子商务站点上的列表页包含包括颜色样本的产品卡。</span><span class="sxs-lookup"><span data-stu-id="6ede4-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![在电子商务列表页上显示为样本的颜色维度的示例](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="6ede4-131">有关如何配置产品维度以使其在站点页面上显示为样本的信息，请参阅[将产品维度值配置为作为样本显示](./dev-itpro/dimensions-swatch.md)。</span><span class="sxs-lookup"><span data-stu-id="6ede4-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ede4-132">其他资源</span><span class="sxs-lookup"><span data-stu-id="6ede4-132">Additional resources</span></span>

[<span data-ttu-id="6ede4-133">模块库概览</span><span class="sxs-lookup"><span data-stu-id="6ede4-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6ede4-134">搜索结果模块</span><span class="sxs-lookup"><span data-stu-id="6ede4-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="6ede4-135">购买框模块</span><span class="sxs-lookup"><span data-stu-id="6ede4-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6ede4-136">将产品维度值配置为作为样本显示</span><span class="sxs-lookup"><span data-stu-id="6ede4-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
