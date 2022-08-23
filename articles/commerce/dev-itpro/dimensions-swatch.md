---
title: 将产品维度值配置为作为样本显示
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce headquarters 中将产品维度值配置为样本。
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.custom: ''
ms.search.industry: Retail
ms.openlocfilehash: e81c1f03eb6387176ca5ce8f751ce53aa0261679
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271982"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a>将产品维度值配置为作为样本显示

[!include [banner](../../includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce headquarters 中将产品维度值配置为样本。 有关产品维度的信息，请参阅[产品维度](../../supply-chain/pim/product-dimensions.md)。

Dynamics 365 Commerce 支持使用尺寸、样式和颜色维度表示产品变型。 产品维度具有易记名称，此名称显示在产品详细信息页 (PDP) 上，让产品变型可以被选择。 这些易记名称的示例包括表示尺寸的“小”、“中”和“大”，以及表示颜色的“黑色”和“棕色”。 但是，如果产品支持很多变体，需要多次选择才能查看每个产品变型的图像。 因此，客户浏览和选择产品变型可能很慢而且繁琐。

当维度在 PDP 上显示为样本时，客户可以直观地预览产品的变体。 他们可以轻松浏览各种颜色、图案和纹理，并可以快速查看产品变体的不同组合。

将维度显示为样本这一功能让 Commerce 能够使用十六进制 (hex) 代码和图像将维度显示为样本。 而且，相似的维度（如颜色）可以在产品列表页上分组。 例如，客户正在搜索蓝色的产品。 如果将各个蓝色维度值分组在一起，搜索结果列表页将显示具有不同蓝色色调的产品。 维度分组显著改进了产品提炼体验，通过单个产品搜索查询帮助客户找到更多产品。

> [!NOTE]
> 从 Dynamics 365 Commerce 版本 10.0.20 开始提供将维度显示为样本功能。

下图显示了一个示例，其中颜色在 Commerce PDP 上显示为样本。

![在产品详细信息页面上显示为样本的颜色的示例。](../dev-itpro/media/swatch_pdp.png)

下图显示了一个示例，其中颜色在 Commerce 搜索结果列表页上显示为样本。

![在搜索结果列表页面上显示为样本的颜色的示例。](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a>在 Commerce headquarters 中启用将维度显示为样本功能

要在 Commerce headquarters 中启用将维度显示为样本功能，转到 **工作区 \> 功能管理**，打开 **启用将维度显示为样本的机制** 功能。 此功能标志启用后，将在 Commerce headquarters 中的相应表中为每个维度添加三个新字段：**Hexcode**、**URL**（图像）、**RefinerGroup**。

## <a name="configure-dimension-values-in-commerce-headquarters"></a>在 Commerce headquarters 中配置维度值

尺寸、样式和颜色维度支持将维度显示为样本功能。 可以在 Commerce headquarters 中为相应维度指定十六进制代码和图像 URL 值。 默认情况下，如果未为维度提供十六进制代码和图像 URL 值，系统将显示维度的易记名称的文本。

可以在以下任一级别进行配置：

- **维度** – 在 Commerce headquarters 中，通过搜索 **颜色**、**尺寸** 或 **样式** 打开维度的页面。 在每个页面上，一个网格将列出维度值。 您可以管理显示顺序、十六进制代码和图像 URL 值。 下图显示了 **颜色** 页上的示例配置。

    ![“颜色”页面上的维度配置的示例。](../dev-itpro/media/swatch_Color.PNG)

- **维度组** – 在 Dynamics 365 Commerce 中，您可以使用 **RefinerGroup** 属性创建维度组。 如果定义了维度组，通过搜索 **颜色组**、**尺寸组** 或 **样式组** 打开相应的页面。 在每个页面上，您可以管理十六进制代码、图像 URL 和提炼组值。 下图显示了 **颜色组** 页上的示例配置。

    ![“颜色组”页面上的维度配置的示例。](../dev-itpro/media/swatch_colorGroup.PNG)

- **产品维度（产品创建期间）** – 创建新产品时，您可以使用 **产品维度** 页输入维度值。 对于现有产品，**Hexcode**、**URL**（图像）和 **RefinerGroup** 字段可能已经设置。 不过，您可以根据需要更改这些值。 下图显示了 **产品维度** 页上的示例配置。

    ![“产品维度”页面上的维度配置的示例。](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> 管理十六进制代码和图像 URL 配置的流程遵照用于管理维度显示顺序的相同模式。

## <a name="configure-dimension-values-by-using-hex-codes"></a>使用十六进制代码配置维度值

对于大多数颜色维度，应在 Commerce headquarters 中的维度页面上提供十六进制代码颜色值。 例如，黑色应具有十六进制代码值 **#00000**。 当 Commerce 呈现站点页面时，十六进制代码由彩色样本表示。

下图显示了使用十六进制代码值配置颜色维度的示例。

![使用十六进制代码的维度配置的示例。](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a>使用图像 URL 配置维度值

有些颜色维度表示图案，而不是纯色。 例如，某个颜色维度可能被描述为“豹”。 在这些情况下，您可以为样本使用发布的图像而不是十六进制代码来更有效地表示颜色维度。

您必须将每个图像上载到 Commerce 站点构建器并进行发布。 然后在 Commerce headquarters 中的相应维度页面上输入发布的图像的图像 URL。 如果选择了某个维度要将其显示为样本，但未定义十六进制代码，Commerce 在呈现页面时将进行图像查找。 如果图像查找失败，Commerce 将显示维度的易记名称的文本。

下图显示了一个示例，其中图像 URL 用于 **颜色** 页上的配置。

![使用图像 URL 的维度配置的示例。](../dev-itpro/media/swatch_color_urls.PNG)

您可以使用媒体模板来定义图像 URL，就像为产品和类别图像定义一样。 当您将图像上载到站点构建器时，文件名约定和文件路径必须一致。

下图显示了一个示例，其中图像 URL 用于媒体模板的配置。

![媒体模板配置的示例。](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a>同时使用十六进制代码和图像 URL 配置维度值

对于大多数颜色维度，您可以同时配置十六进制代码和图像 URL。 Commerce 呈现回退逻辑将自动查找十六进制代码或图像 URL 来显示颜色样本。 同时使用十六进制代码和图像 URL 配置颜色维度，当颜色数量较多时，可以帮助简化图像管理。

下图显示了一个示例，其中十六进制代码和图像 URL 同时用于 **颜色** 页上的配置。

![同时使用十六进制代码和图像 URL 的维度配置的示例。](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a>配置提炼组

当您为维度值定义十六进制代码或图像 URL 时，您还可以为 **RefinerGroup** 字段指定值。 此字段定义应在提炼体验中用于对相似维度值进行分组的维度。

例如，如果您的颜色维度值是“蓝色”、“蓝色格子”、“涂蓝色”和“深蓝色”，每个值都映射到不同的十六进制代码或图像 URL。 因此，每个值都将在相应产品的 PDP 和产品卡上显示为不同的颜色。 但是，如果您将所有这些颜色维度值映射到 **蓝色** 的 **RefinerGroup** 值，搜索“蓝色”产品将生成具有“蓝色”、“蓝格子”、“涂蓝色”和“深蓝色”维度颜色值的产品的列表页搜索结果。

下图中的示例显示了 Commerce headquarters 中 **颜色** 和 **RefinerGroup** 属性之间的关系。

![优化组管理的示例。](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a>在 Commerce 站点构建器中管理图像

如果将图像 URL 用于任何维度值，则必须将相应的图像上载到 Commerce 站点构建器。 每个图像的位置应与在 Commerce headquarters 中为该图像定义的文件名和文件夹路径匹配。 图像文件必须上载到站点构建器中的相应类别位置。 例如，颜色图像必须上载到 **颜色** 类别文件夹。 有关如何将图像上载到站点构建器的详细信息，请参阅[上载图像](../dam-upload-images.md)。

下图显示了一个示例，其中 **上载文件** 对话框用于将图像上载到站点构建器媒体库。 可供选择的 **尺寸**、**颜色** 和 **样式** 类别突出显示。

![上传到站点构建器媒体库期间的图像文件类别的示例。](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a>在电子商务站点页面上启用样本显示

您必须在 Commerce headquarters 中配置维度站点设置，然后样本才能够显示在需要选择维度的电子商务站点页面（如 PDP 和列表页）上。 有关详细信息，请参阅[应用维度的站点设置](../dimension-settings.md)。

此外，您应该为搜索结果模块启用 **在搜索结果中包括产品属性** 属性。 如果您的站点使用自定义类别页面，您应该更新在这些页面上使用的搜索结果模块，以启用 **在搜索结果中包括产品属性** 属性。 有关详细信息，请参阅[搜索结果模块](../search-result-module.md)。

## <a name="inventory-awareness-on-swatches"></a>样本库存意识

样本具有显示产品变型颜色或维度的库存可用性的可选功能。 例如，一种产品以多种尺寸出售，但某些尺寸却缺货。 在这种情况下，系统会以不同方式呈现库存不足产品的样本以指示它们缺货。 此功能有助于减少确定产品可用性所需的客户单击次数。

样本库存可用性功能可以配置为在 PDP 和显示样本的搜索或类别列表页面上使用。 若要激活它，您必须在 [媒体库模块](../media-gallery-module.md)中将 **更新维度选择的媒体** 设置为 **True**。 该设置允许在选择维度时更新媒体库图像。 

> [!IMPORTANT]
> 样本库存可用性功能从 Commerce 版本 10.0.21 版开始可用。 它要求安装 Commerce 模块库包版本 9.31。

下图显示了有关 PDP 大小样本的库存意识的示例。

![有关 PDP 大小样本的库存意识示例](../dev-itpro/media/swatch_inventory.png)

## <a name="display-swatches-in-pos-and-other-channels"></a>在 POS 和其他渠道中显示样本

Commerce 目前没有支持在销售点 (POS) 和其他渠道中显示样本的现成实现。 不过，您可以将样本显示功能作为扩展来实现，因为渠道 API 返回呈现样本所需的十六进制代码和图像 URL。

## <a name="additional-resources"></a>其他资源

[搜索结果模块](../search-result-module.md)

[应用维度的站点设置](../dimension-settings.md)

[产品维度](../../supply-chain/pim/product-dimensions.md)

[上传图像](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
