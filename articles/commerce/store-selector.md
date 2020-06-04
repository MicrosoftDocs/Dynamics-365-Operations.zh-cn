---
title: 商店选择器模块
description: 此主题介绍商店选择器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378200"
---
# <a name="store-selector-module"></a>商店选择器模块

[!include [banner](includes/banner.md)]

此主题介绍商店选择器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

商店选择器模块用于“在线购买，店内提货”(BOPIS) 客户方案。 它显示可以提走产品的商店列表，以及每个商店的商店营业时间和产品库存。

商店选择器模块需要产品的上下文和查找商店的搜索位置。 在没有搜索位置的情况下，如果客户给出同意表示，搜索位置将默认为客户的浏览器位置。 此模块有一个输入框，允许客户输入位置（邮政编码或城市和州/省）来查找附近的商店。

商店选择器模块与 Bing 地图地理编码应用程序编程接口 (API) 集成在一起，以将位置转换为纬度和经度。 必须提供 Bing 地图 API 密钥，并且必须将其添加到 Dynamics 365 Commerce 内的“Commerce 共享参数”页面中。

商店选择器模块可以添加到“产品详细信息”页面 (PDP) 上的购买框模块中，来显示可提走产品的商店。 也可以将其添加到购物车模块。 当添加到购物车模块时，商店选择器模块将显示每个购物车行项的提货选项。 另外，使用自定义编码，可以通过扩展和自定义将此模块添加到其他页面或模块。

为了使 BOPIS 方案正常工作，应使用“客户提货”交货模式配置产品。 否则，此模块将不会在相应页面上显示。 有关如何配置交货模式的详细信息，请参阅[设置交货模式](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)。

下图显示了 PDP 上使用的商店选择器模块的示例。

![商店选择器模块的示例](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>电子商务中商店选择器模块的使用

- 商店选择器模块可以在“产品详细信息”页面 (PDP) 上用于查找附近可提走产品的商店。
- 商店选择器模块可以在购物车页面上用于查找附近可提走购物车中产品的商店。

## <a name="store-selector-module-properties"></a>商店选择器模块属性

| 属性名称             | 值                 | 说明 |
|---------------------------|-----------------------|-------------|
| 搜索半径 | 数值 | 定义商店的搜索半径，以英里为单位。 如果未指定任何值，则使用默认的 50 英里搜索半径。|
|服务条款 | URL    |  Bing 地图服务需要的服务条款 URL。 |

## <a name="add-a-store-selector-module-to-a-page"></a>向页面添加商店选择器模块

商店选择器模块需要产品的上下文，因此只能在购买框和购物车模块中使用。 商店选择器模块在这些模块之外不起作用。

- 有关如何将商店选择器模块添加到购买框模块的信息，请参阅[购买框模块](add-buy-box.md)。 
- 有关如何将商店选择器模块添加到购物车模块的信息，请参阅[购物车模块](add-cart-module.md)

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[快速浏览 PDP](quick-tour-pdp.md)

[快速浏览购物车和结帐](quick-tour-cart-checkout.md)

[设置交货方式](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[管理组织的必应地图](dev-itpro/manage-bing-maps.md)
