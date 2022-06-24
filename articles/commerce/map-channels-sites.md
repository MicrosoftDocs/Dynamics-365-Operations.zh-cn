---
title: 将渠道映射到电子商务站点
description: 本文介绍 Microsoft Dynamics 365 Commerce 中可针对大多数其他业务需求外推的一些更常见的渠道映射方案。
author: samjarawan
ms.date: 05/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 94c43df26e8d6e55a5b6d459b65066d5873e1063
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902755"
---
# <a name="map-channels-to-e-commerce-sites"></a>将渠道映射到电子商务站点

本文介绍 Microsoft Dynamics 365 Commerce 中可针对大多数其他业务需求外推的一些更常见的渠道映射方案。

Dynamics 365 Commerce 支持将具有一组已配置产品、价格和折扣的[在线渠道](#channels)映射到[电子商务站点](#e-commerce-sites)客户体验的许多业务方案。

本文介绍以下方案：

- **具有单一电子商务站点体验的单语言渠道。** 例如，此方案可能涉及为美国英语市场配置的单一品牌站点。
- **具有单一本地化站点体验的多语言渠道。** 例如，此方案可能涉及为加拿大配置的具有法语和英语语言支持的单一品牌站点。 在此方案中，选择不同语言的用户具有相同的站点体验，但语言被本地化为每个用户选择的语言。
- **具有每种语言的不同站点体验的多语言渠道。** 例如，此方案可能涉及为加拿大配置的具有法语和英语语言支持的单一品牌站点。 在此方案中，每种语言都有唯一的站点体验。
- **具有单一本地化站点体验的多个渠道（单语言和/或多语言）。** 例如，此方案可能涉及为澳大利亚和新西兰配置的单一品牌站点。 在此方案中，这两个国家/地区具有相同的英语站点体验，但每个国家/地区都配置了不同的产品、货币、价格、折扣和运输方式。
- **具有每个渠道的不同站点体验的多个渠道（单语言和/或多语言）。** 例如，此方案可能涉及为澳大利亚、加拿大和德国配置的多种语言单一品牌站点。 在此方案中，每个国家/地区都具有侱的站点体验，并且该体验配置了不同的产品、货币、价格、折扣和运输方式。

## <a name="channels"></a>渠道

渠道（也称为在线商店或在线渠道）表示在线电子商务店面，用于映射产品、定价、折扣、语言、付款方式、交货模式、履行中心和在线体验的其他方面，这些内容都将提供给您的电子商务客户。 渠道在 Commerce Headquarters 中创建和管理，并映射到单个[法人](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json#legal-entities)。 法人通常位于需要对渠道进行税务报告的单个国家/地区，并且只能配置一种货币。

有关渠道的详细信息，请参阅[渠道概览](channels-overview.md)。 有关如何创建在线渠道的详细信息，请参阅[设置在线渠道](channel-setup-online.md)。

Commerce Headquarters 中的以下示例图显示了选择演示数据选项时使用 Dynamics 365 Commerce 部署的默认在线渠道。

![Commerce Headquarters 中的默认演示数据渠道。](media/channel-mapping-1.png)

## <a name="e-commerce-sites"></a>电子商务站点

电子商务站点包含一组供客户用来浏览和购物的站点页面。 电子商务站点在 Commerce 站点生成器中进行管理。

有关如何在站点生成器中创建和管理站点的详细信息，请参阅[电子商务站点概览](online-store-overview.md)。

## <a name="common-channel-mapping-scenarios"></a>公共渠道映射方案

Dynamics 365 Commerce 支持各种渠道映射方案。 接下来的渠道映射方案只是所有可能的渠道映射方案的子集。 它们旨在作为指南，帮助您计划您拥有的任何唯一业务方案。 包含在 Dynamics 365 Commerce 演示数据中的虚构的 Adventure Works 体育用品商店用作每个方案的示例。

### <a name="single-language-channel-that-has-a-single-e-commerce-site-experience"></a>具有单一电子商务站点体验的单语言渠道

在最基本的方案中，单个渠道具有用于在单个市场中进行销售的单一语言。 此方案的一个示例是仅为美国英语市场设置的 Adventure Works 在线商店。

以下示例图显示了 Commerce headquarters 中的渠道配置。 在此配置中，在线渠道仅支持用于纳税申报的单一语言 (**en-us**)、单一货币 (**USD**) 和单个业务实体 (**usrt**)。

![Commerce Headquarters 中突出显示了 Adventure Works 在线商店的法人、货币和语言值。](media/channel-mapping-3.png)

单个在线渠道可以映射到站点生成器中的单个电子商务站点。 有关如何创建新站点并将其映射到渠道的信息，请参阅本文的[在站点生成器中将渠道映射到站点](#map-a-channel-to-a-site-in-site-builder)一节。

### <a name="multi-language-channel-that-has-a-single-localized-site-experience"></a>具有单一本地化站点体验的多语言渠道

在此方案中，单个渠道支持多种语言。 因此，可以在 Commerce Headquarters 中本地化产品名称、描述和属性。 若要提供完全本地化的站点体验，也可以在 Commerce 站点生成器中本地化站点上的市场营销内容。

此方案的限制是，单个渠道只能配置一种货币、一个法人以及一组产品和价格。 此配置最适用于具有单一货币和多种语言、单个法人以及一组产品和价格的国家/地区（例如，采用英语和法语语言的加拿大）。

可以为渠道中的每种语言配置其自己的域名。 例如，可以为加拿大英语版本配置 `www.adventure-works.ca` 域，可以为加拿大法语版本配置 `www.adventure-works-fr.ca` 域。 或者，可以在单个域中配置渠道中的不同语言，然后可以为每种语言使用其他路径。 例如，可以为加拿大英语版本配置 `www.adventure-works.ca` 域，然后可以为加拿大法语版本使用 `www.adventure-works.ca/fr` 路径。 还可以启用[地理检测](geo-detection-redirection.md)，以便根据用户的位置自动将用户重定向到正确的站点。

有关如何使客户能够在语言之间手动切换的信息，请参阅本文的[添加并配置站点选取器模块](#add-and-configure-the-site-picker-module)一节。 有关如何自定义本地化页面和片段的信息，请参阅[管理具有多种渠道和语言的站点内容](#manage-site-content-that-has-multiple-channels-and-languages)部分。

### <a name="multi-language-channel-that-has-a-different-site-experience-per-language"></a>具有每种语言的不同站点体验的多语言渠道

您可能更喜欢单个频道支持多种语言但每种语言都会呈现完全不同的站点体验的方案。 实现此方案的建议方法是在单个站点上使用[页面变型](#implement-page-variants-for-each-language)。

另一种方法是在站点生成器中为每种语言创建一个新的电子商务站点，然后将每个站点映射到单个在线渠道和语言。 结果将是一个单一的在线渠道，该渠道映射到多个电子商务站点，每种语言都有一个电子商务站点。 此多站点方法需要额外的管理资源，因为在站点生成器中将有多个站点需要管理。

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-single-localized-site-experience"></a>具有单一本地化站点体验的多个渠道（单语言和/或多语言）

品牌站点可能需要每个区域有多个在线渠道来支持单个站点中每个渠道的不同货币、产品集和价格集。 例如，Adventure Works 站点可能有一个面向加拿大市场的多语言在线渠道、一个面向美国市场的单语言渠道，以及一个面向德国市场的单语言渠道。 在此方案中，将为特定于地区的法人配置每个在线渠道，并且该渠道可以具有其他渠道所具有的相同产品集、这些产品的子集或其他一组产品。 每个渠道也将有自己的区域货币价格、税收、折扣和运输方式。

在此方案中，可以为每个市场配置其自己的域名。 例如，可以为美国市场配置 `www.adventure-works.com` 域，可以为德国市场配置 `www.adventure-works.de` 域。 或者，可以将每个市场配置为使用其他路径。 例如，可以为美国市场配置 `www.adventure-works.com` 域，然后可以将 `www.adventure-works.com/de` 路径用于德国市场。 还可以启用[地理检测](geo-detection-redirection.md)，以便根据用户的区域自动将用户重定向到正确的站点。

您可能还希望您的站点提供一个下拉列表，以让用户手动切换到特定市场。 有关详细信息，请参阅本文的[添加并配置站点选取器模块](#add-and-configure-the-site-picker-module)一节。

有关如何在单个站点上配置多个渠道的信息，请参阅[在电子商务站点上配置多个渠道](#configure-multiple-channels-on-an-e-commerce-site)部分。

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-different-site-experience-per-channel"></a>具有每个渠道的不同站点体验的多个渠道（单语言和/或多语言）

您可能希望在不同区域为单个品牌提供多个渠道，并且您可能希望每个区域都有不同的站点体验。 实现此方案的方法有两种：

- 使用[页面变型](#implement-page-variants-for-each-language)。
- 在站点生成器中为每个在线渠道配置不同的站点，然后将每个站点映射到不同的在线渠道和语言。 此方法需要额外的管理资源，因为在站点生成器中将有多个站点需要管理。

## <a name="cross-channel-sharing"></a>跨渠道共享

当单个站点上的多个渠道可以共享内容时，跨渠道共享非常有用。 例如，具有在一个站点下分组的多个品牌和店面的零售商可以在一些或所有店面之间共享某些内容。 共享的内容可以包括有关条款和条件、付款期、运输方式和常见问题 (FAQ) 的页面。 有关详细信息，请参阅[启用和使用跨渠道共享](cross-channel-sharing.md)。

## <a name="map-a-channel-to-a-site-in-site-builder"></a>在站点生成器中将渠道映射到站点

有多种方法可以创建和配置站点以使用不同的在线渠道。

### <a name="create-a-new-site"></a>创建新站点

您可以通过转到 **站点** 列表页并选择 **新站点**，在站点生成器中创建一个全新的站点。 然后，在显示的 **新站点** 对话框中，您可以选择站点的默认在线渠道和语言，如以下示例图中所示。

![在站点生成器中创建新渠道。](media/channel-mapping-4.png)

您以这种方式创建的站点将是空站点，并且不会包含任何站点页面（例如，主页、类别页面和产品页面）。

有关详细信息，请参阅[创建电子商务站点](create-ecommerce-site.md)。

### <a name="create-a-new-site-by-using-the-site-copy-operation"></a>使用站点复制操作创建新站点

更好的做法是从 Commerce 模块库中提供的一个起始站点（例如 Fabrikam 或 Adventure Works 站点）的副本开始，而不是上一节中描述的创建全新空站点。

要复制现有站点，请转到站点生成器中的 **站点** 列表页，然后选择 **复制站点**。 然后，在显示的 **复制站点** 对话框中，您可以选择源站点并指定目标站点的名称。

此时，您还无法选择站点的默认在线渠道和语言。 但是，您可以在完成站点复制操作后配置这些属性。 当您第一次在站点生成器的 **站点** 列表页上选择站点时，将显示 **设置站点** 对话框，您可以在其中选择默认渠道和语言。

有关站点复制操作的详细信息，请参阅[复制电子商务站点](copy-ecommerce-site.md)。

### <a name="manage-an-existing-site-channel"></a>管理现有站点渠道

为站点配置渠道后，您可以在站点生成器内的 **站点设置 \> 渠道** 中管理和更新选定站点内的渠道，如下面的示例图所示。

![在站点生成器中管理渠道映射。](media/channel-mapping-7.png)

## <a name="support-multiple-sites-in-a-single-tenant"></a>支持单个租户中的多个站点

许多品牌站点可以在单个租户中共存。 以下示例图显示了三个不同的品牌站点（Adventure Works、Adventure Works Business 和 Fabrikam），每个站点都映射到不同的单个在线渠道。

![站点生成器中的站点列表。](media/channel-mapping-8.png)

## <a name="configure-a-single-domain-name-with-paths-for-multiple-sites"></a>为多个站点配置具有路径的单个域名

单个域名可用于多个站点，然后路径可用于分开站点或语言。 例如，为两个不同的电子商务站点配置了 `www.mycompany.com` 域：一个用于 Fabrikam，一个用于 Adventure Works。 在这种情况下，默认路径（`www.mycompany.com`，也称为空白路径）可用于 Fabrikam 站点，另一个路径（例如 `www.mycompany.com/adventureworks`）可用于 Adventure Works 站点。 另一个选项是使用自定义路径（例如 `www.mycompany.com/fabrikam`），而不是也对 Fabrikam 站点使用默认路径。

或者，也可以将其他域名用于每个站点（例如 `www.adventure-works.com`和 `www.fabrikam.com`）。 然后，可将路径用于不同的语言或区域（例如，将 `www.adventure-works.com/fr-ca` 用于加拿大法语）。

## <a name="configure-multiple-languages-on-a-site"></a>在站点上配置多种语言

可以在站点生成器内的 **站点设置 \> 渠道** 中为电子商务站点配置语言。 在以下示例图中，已使用路径的区域设置配置了每种语言，因此每种语言都有一个唯一的 URL。

![在站点上配置了多种语言。](media/channel-mapping-10.png)

若要添加新的渠道语言，请转到 **站点设置 \> 渠道**，然后选择渠道链接。 在右侧显示的窗格中，选择 **添加区域设置** 以选择要添加的渠道和区域设置。 然后指定要用于所选渠道的路径。

### <a name="add-and-configure-the-site-picker-module"></a>添加和配置站点选取器模块

为站点配置了多种语言和/或渠道后，您可能希望将语言选择器添加到站点页面标题中，以便用户可以手动选择他们的语言或国家/地区。 模块库[标题模块](author-header-module.md)内置支持功能，用户可以使用[站点选取器模块](site-selector.md)选择语言。 站点选取器模块可以添加到标题片段中的标题模块。

有关如何添加和配置站点选取器模块的更多信息，请参阅[站点选取器模块](site-selector.md)。

### <a name="implement-page-variants-for-each-language"></a>为每种语言实施页面变型

在此方案中，只有一个渠道，但存在多种语言。 您可以根据所选语言更改页面的外观，方法是为其创建一个页面变型。 然后，您可以将本地化内容添加到该变型中。

当您在站点生成器中打开页面并选择右上角显示当前渠道和语言的链接时，会出现一个渠道和语言选取器，如下面的示例图所示。 如果您要替代当前语言的页面，请选择其他区域设置，然后选择 **更改**。 如果您要[管理具有多个渠道和语言的站点](#manage-site-content-that has-multiple-channels-and-languages)，则也可以更改渠道。

![在站点生成器中更改页面的语言。](media/channel-mapping-14.png)

如果尚未创建所选页面或片段的变型，您会收到一条警告消息，如下面的示例图所示。 在此情况下，请选择消息文本中的 **创建页面变型** 链接。 出现的对话框提供了允许您从现有变型的副本开始或从模板创建全新页面的选项。

![提示在站点生成器中创建页面变型](media/channel-mapping-16.png)

如果未创建变型，则将呈现原始页面，并显示来自 Commerce Headquarters 的模块字符串和产品信息的相应语言。 但是，如果已直接在默认页面模块中指定文本（如页面标题或其他市场营销内容），则该文本的字符串将仍为原始语言。

无需手动创建每个页面和片段，您可以将每个页面和片段导出到 XML 本地化交换文件格式 (XLIFF) 文件，然后发送该文件进行本地化。 在本地化了每个 XLIFF 之后，可以将其作为本地化页面变型导入。 要从站点生成器中的页面或片段导出 XLIFF 文件，或将 XLIFF 文件导入页面或片段，请在命令栏上选择 **本地化**。 然后选择 **导出 XLIFF** 或 **导入 XLIFF**，如以下示例图中所示。

![正在导入或导出 XLIFF 格式的页面或片段。](media/channel-mapping-18.png)

## <a name="manage-site-content-that-has-multiple-channels-and-languages"></a>管理具有多个渠道和语言的站点内容

具有多个渠道和/或语言的站点存储了每个页面的唯一变体以及每个渠道和语言组合的片段。 此行为使页面变型能够包含本地化数据，但也使您能够灵活地更改特定变型的页面外观。

有关如何使用页面变型的信息，请参阅本文的[为每种语言实施页面变型](#implement-page-variants-for-each-language)一节。

## <a name="configure-multiple-channels-on-an-e-commerce-site"></a>在电子商务站点上配置多个渠道

通过转到 **站点设置 \> 渠道** 并选择 **添加渠道**，您可以在站点生成器中将渠道添加到电子商务站点。 然后，在出现的 **添加渠道** 对话框中，您可以选择在线渠道和默认区域设置。

## <a name="additional-resources"></a>其他资源

[渠道概览](channels-overview.md)

[设置在线渠道](channel-setup-online.md)

[组织和组织层次结构概览](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md)

[设置地理检测和重定向](geo-detection-redirection.md)

[启用和使用跨渠道共享](cross-channel-sharing.md)

[创建电子商务站点](create-ecommerce-site.md)

[复制电子商务站点](copy-ecommerce-site.md)

[站点选取器模块](site-selector.md)
