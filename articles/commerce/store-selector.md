---
title: 商店选择器模块
description: 此主题介绍商店选择器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 74dbad4cb348f19b51ba8b84a1cd41fc5049708e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006327"
---
# <a name="store-selector-module"></a>商店选择器模块

[!include [banner](includes/banner.md)]

此主题介绍商店选择器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

客户可以在在线购买后使用商店选择器模块在选定商店提货。 在 Commerce 版本 10.0.13 中，商店选择器模块还包括其他功能，可以展示显示附近商店的 **查找商店** 页面。

商店选择器模块允许用户输入位置（城市、省/自治区/直辖市、地址等）来在搜索半径内搜索商店。 首次打开此模块时，它使用客户的浏览器位置来查找商店（如果确认同意）。

## <a name="store-selector-module-usage-in-e-commerce"></a>电子商务中商店选择器模块的使用

- 可以在产品详细信息页面 (PDP) 使用商店选择器模块来选择提货商店。
- 可以在购物车页面使用商店选择器模块来选择提货商店。
- 商店选择器模块可以在显示所有可选择商店的独立页面上使用。

## <a name="bing-maps-integration"></a>必应地图集成

商店选择器模块与[必应地图 REST 应用程序编程接口 (API)](https://docs.microsoft.com/bingmaps/rest-services/) 集成来使用必应的地理编码和自动建议功能。 必须提供必应地图 API 密钥，并且必须将其添加到 Commerce headquarters 内的共享参数页面中。 地理编码 API 用于将位置转换为纬度和经度值。 与自动建议 API 的集成用于在用户在搜索字段中输入位置时显示搜索建议。

对于自动建议 REST API，您必须确保根据站点的内容安全策略 (CSP) 允许以下 URL。 通过在站点的各个 CSP 指令中添加允许的 URL（例如，**img-src**），在 Commerce 站点构建器中完成此设置。 有关详细信息，请参阅[内容安全策略](manage-csp.md)。 

- 对于 **connect-src** 指令，添加 **&#42;.bing.com**。
- 对于 **img-src** 指令，添加 **&#42;.virtualearth.net**。
- 对于 **script-src** 指令，**添加 &#42;.bing.com、&#42;.virtualearth.net**。
- 对于 **script style-src** 指令，添加 **&#42;.bing.com**。
 
## <a name="pickup-in-store-mode"></a>店内提货模式

商店选择器模块支持 **店内提货** 模式，其显示可提货的商店列表。 它还在列表中显示每个商店的营业时间和产品库存。 如果产品的交货方式设置为在所选商店 **提货**，商店选择器模块将需要产品的上下文来呈现产品可用性并允许用户将产品添加到购物车。 有关详细信息，请参阅[库存设置](inventory-settings.md)。 

商店选择器模块可以添加到购买框模块中，来显示可提货的商店。 也可以将其添加到购物车模块。 如果是这种情况，商店选择器模块将显示购物车中每个行项的提货选项。 商店选择器模块还可以通过扩展和自定义添加到其他页面或模块。

为了使此方案正常工作，产品应配置为使用 **提货** 交货方式。 否则，此模块不会在产品页面上显示。 有关如何配置交货方式的详细信息，请参阅[设置交货方式](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)。

下图显示了 PDP 上使用的商店选择器模块的示例。

![PDP 上使用的商店选择器模块的示例](./media/BOPIS.PNG)

> [!NOTE]
> 在版本 10.0.16 及更高版本中，可以启用一项新功能，该功能让组织可以为客户定义多个提货交货方式选项。  如果启用此功能，商店选择器和电子商务的其他模块将得到增强，可以允许购物者从可能提供的多个提货交货选项（如果配置）中进行选择。  要了解有关此功能的详细信息，请参阅[本文档](https://docs.microsoft.com/dynamics365/commerce/multiple-pickup-modes)。 

## <a name="find-stores-mode"></a>查找商店模式

商店选择器模块还支持 **查找商店** 模式。 此模式可用于创建显示可选择商店及其信息的商店位置页面。 在此模式下，商店选择器模块可以在没有产品上下文的情况下工作，并可以在任何站点页面上用作独立模块。 此外，如果为模块打开了相关设置，用户可以选择一个商店作为其首选商店。 当选择一个商店作为用户的首选商店时，该商店 ID 将保留在浏览器 Cookie 中。 因此，用户必须接受 Cookie 同意消息。

下图显示了与商店位置页面上的地图模块一起使用的商店选择器模块的示例。

![商店位置页面上的商店选择器模块和地图模块的示例](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a>呈现地图

商店选择器模块可与地图模块一起使用，来在地图上显示商店位置。 有关地图模块的详细信息，请参阅[地图模块](map-module.md)

## <a name="store-selector-module-properties"></a>商店选择器模块属性

| 属性名称 | 值 | 说明 |
|---------------|-------|-------------|
| 标题 | 文本 | 模块的标题。 |
| 模式 | **查找商店** 或 **店内提货** | **查找商店** 模式显示可选择的商店。 **店内提货** 模式可让用户选择要提货的商店。 |
| 样式 | **对话** 或 **内联** | 此模块可以内联或在对话框中呈现。 |
| 设置为首选商店 | **True** 或 **False** | 当此属性设置为 **True**，用户可以设置首选商店。 此功能需要用户接受 Cookie 同意消息。 |
| 显示所有商店 | **True** 或 **False** | 当此属性设置为 **True** 时，用户可以绕过 **搜索半径** 属性，查看所有商店。 |
| 自动建议选项：最多结果 | 数值 | 此属性定义可通过必应自动建议 API 显示的自动建议结果的最大数量。 |
| 搜索半径 | 数值 | 此属性定义商店的搜索半径，以英里为单位。 如果未指定任何值，则使用默认的 50 英里搜索半径。 |
| 服务条款 | URL |  此属性指定使用必应地图服务所需的服务条款 URL。 |

## <a name="add-a-store-selector-module-to-a-page"></a>向页面添加商店选择器模块

对于 **店内提货** 模式，此模块只能在 PDP 和购物车页面使用。 您必须在模块的属性窗格中将模式设置为 **店内提货**。

- 有关如何将商店选择器模块添加到购买框模块的信息，请参阅[购买框模块](add-buy-box.md)。 
- 有关如何将商店选择器模块添加到购物车模块的信息，请参阅[购物车模块](add-cart-module.md)

要将商店选择器模块配置为在商店位置页面显示可选择的商店（如本主题前面的插图中所示），请执行以下步骤。

1. 转到 **模板**，选择 **新建** 创建新模板。
1. 在 **新建模板** 对话框的 **模板名称** 下，输入 **市场营销模板**，然后选择 **确定**。
1. 选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。
1. 转到 **页面**，选择 **新建** 创建新页面。
1. 在 **选择模板** 对话框中，选择 **市场营销模板** 模板。 在 **页面名称** 下，输入 **商店位置**，然后选择 **确定**。
1. 在新页面的 **主** 插槽，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **容器** 模块，然后选择 **确定**。
1. 在 **容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **2 列容器** 模块，然后选择 **确定**。
1. 在模块的属性窗格中，将 **宽度** 值设置为 **填充容器**。
1. 将 **超小查看端口配置** 值设置为 **100%**。
1. 将 **小查看端口配置** 值设置为 **100%**。
1. 将 **中等查看端口配置** 值设置为 **33% 67%**。
1. 将 **大查看端口配置** 值设置为 **33% 67%**。
1. 在 **2 列容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **商店选择器** 模块，然后选择 **确定**。
1. 在模块的属性窗格中，将 **模式** 值设置为 **查找商店**。
1. 设置 **搜索半径** 值，以英里为单位。
1. 根据您的需要设置其他属性，如 **设置为首选商店**、**显示所有商店** 和 **启用自动建议**。
1. 在 **2 列容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。
1. 在 **添加模块** 对话框中，选择 **地图** 模块，然后选择 **确定**。
1. 在模块的属性窗格中，根据需要设置任何其他属性。
1. 选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。
 
## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[快速浏览 PDP](quick-tour-pdp.md)

[快速浏览购物车和结帐](quick-tour-cart-checkout.md)

[设置交货方式](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[为您的组织管理必应地图](dev-itpro/manage-bing-maps.md)

[必应地图 REST API](https://docs.microsoft.com/bingmaps/rest-services/)

[地图模块](map-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]