---
title: 地图模块
description: 此主题介绍地图模块以及如何在 Microsoft Dynamics 365 Commerce 中配置该模块。
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b8c3ab0653fd5e3561d0bfbe85624d912756e2be
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794179"
---
# <a name="map-module"></a>地图模块

[!include [banner](includes/banner.md)]


此主题介绍地图模块以及如何在 Microsoft Dynamics 365 Commerce 中配置该模块。

地图模块在使用[必应地图 V8 Web 控件](https://docs.microsoft.com/bingmaps/v8-web-control/)呈现的交互式地图上显示商店位置。 必须提供必应地图 API 密钥，并且必须将其添加到 Commerce headquarters 内的共享参数页面中。 地图模块提供不同的视图，如道路、空中和街边，用户可以选择这些视图来查看地图位置。 它们还允许进行交互，如缩放和使用用户的位置。

将地图模块与商店选择器模块结合使用可以确定必须在地图上呈现的商店的地理位置。 当用户在站点页面上的其中一个模块中选择商店时，商店选择器和地图模块进行交互。 除了与商店选择器模块进行交互外，地图模块还可以针对其他场景扩展。 但是，需要对模块进行自定义。

> [!NOTE]
> 此地图模块在 Dynamics 365 Commerce 10.0.13 版本中提供。

下图显示了商店位置页面上使用的地图块模块的示例。

![商店选择器模块的示例](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>模块属性

| 属性名称             | 值                 | 说明 |
|---------------------------|-----------------------|-------------|
| 标题 | 文本 | 模块的标题。 |
| 图钉选项：默认图标 | 头像 | 用于地图上显示的商店的图钉符号图像。 |
| 图钉选项：活动图标 | 头像 | 用于在地图上选择的商店的图钉符号图像。 |
| 图钉选项：默认图标颜色 | 字符串 | 地图上图钉符号颜色的文本或十六进制值。 |
| 图钉选项：活动图标颜色 | 字符串 | 地图上所选图钉符号的颜色的文本或十六进制值。 |
| 显示索引 | **True** 或 **False** | 如果将此属性设置为 **True**，表示商店的每个图钉符号将显示一个索引。 此索引将与商店选择器模块显示的列表视图中的索引匹配。 |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>将允许的映射 URL 添加到站点的内容安全策略指令中

若要使地图模块与必应地图交互，您必须确保根据站点的内容安全策略 (CSP) 允许以下映射 URL。 通过在各个站点 CSP 指令中添加允许的 URL（例如，**img-src**），在 Commerce 站点构建器中完成此设置。 有关详细信息，请参阅[内容安全策略](manage-csp.md)。 

- 对于 **connect-src** 指令，添加 **&#42;.bing.com**。
- 对于 **img-src** 指令，添加 **&#42;.virtualearth.net**。
- 对于 **script-src** 指令，添加 **&#42;.bing.com、&#42;.virtualearth.net**。
- 对于 **script style-src** 指令，添加 **&#42;.bing.com**。

## <a name="add-a-map-module-to-a-page"></a>向页面添加地图模块

有关如何在页面上配置地图模块的详细信息，请参阅[商店选择器模块](store-selector.md)。 
 
## <a name="additional-resources"></a>其他资源

[模块库概述](starter-kit-overview.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[商店选择器模块](store-selector.md)

[为您的组织管理必应地图](./dev-itpro/manage-bing-maps.md)

[必应地图 V8 Web 控件](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]