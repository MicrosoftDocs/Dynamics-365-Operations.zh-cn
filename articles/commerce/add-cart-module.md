---
title: 购物车模块
description: 此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025428"
---
# <a name="cart-module"></a>购物车模块


[!include [banner](includes/banner.md)]

此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

购物车模块用于显示客户继续结帐之前已添加到购物车中的物品。 例如，其中包含已添加到购物车的所有项和订单摘要。 它还允许客户应用或删除促销代码。

购物车模块支持登录结帐和访客结帐。 它还支持**返回购物**链接。 您可以在**站点设置 \> 扩展 \> 路由**中为此链接配置路由。

购物车模块基于购物车 ID 显示数据。 购物车 ID 是整个站点中可用的浏览器 cookie。

## <a name="cart-module-properties-and-slots"></a>购物车模块属性和插槽

购物车模块有一个**标题**属性，此属性可以设置为**购物袋**和**购物车中的商品**之类的值。 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>购物车模块中可使用的模块

- **文本块** – 此模块支持购物车模块中的自定义消息。 消息由内容管理系统 (CMS) 驱动。 可以添加任何消息，如“订单问题请致电 1-800-Fabrikam”。
- **商店选择器** – 此模块显示附近可提货的商店的列表。 它使用户可以输入位置来查找附近的商店。 商店选择器模块与 Bing 地图地理编码应用程序编程接口 (API) 集成在一起，以将位置转换为纬度和经度。 必须提供 Bing 地图 API 密钥，并且必须将其添加到 Dynamics 365 Retail 内的“零售共享参数”页面中。 该模块支持**搜索半径**和**服务条款链接**这两个属性。 **搜索半径**属性定义以英里为单位的商店搜索半径。 如果未指定任何值，则使用默认搜索半径（50 英里）。 如果使用了 Bings 地图或任何外部服务，**服务条款链接**属性可用于提供指向服务条款的链接。 Bing 地图服务需要一个服务条款链接。 

## <a name="cart-module-settings"></a>购物车模块设置

购物车框模块中有可在**站点设置 \> 扩展**中配置的以下设置：

- **最大数量** – 此属于用于指定可以添加到购物车的每种项的最大数量。 例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。
- **库存检查** – 如果此值设置为 **True**，则只有在购买框模块确信某种项有现货时，才能将此项添加到购物车中。 将在项发货时和在商店中提货时执行库存检查。 如果此值设置为 **False**，则向购物车添加项和下订单前，不进行库存检查。
- **库存缓冲区** – 此属性用于指定库存的缓冲区号。 库存会被实时维护，如果多位客户下订单，则很难维持精确的库存计数。 进行库存检查时，如果库存比缓冲区数量少，则将产品视为库存不足。 因此，当通过多个渠道快速进行销售，导致库存计数无法充分同步时，出售库存不足的项的风险较低。
- **返回购物** – 该属性用于指定**返回购物**链接的路由。 可以在站点级别配置此路由。 通过这种配置，零售商可以将客户带回到站点上的主页或任何其他页面。

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit 交互

购物车模块使用 Commerce Scale Unit API 检索产品信息。 浏览器 cookie 中的购物车 ID 用于从 Commerce Scale Unit 检索所有产品信息。

## <a name="add-a-cart-module-to-a-page"></a>向页面添加购物车模块

若要向新页面添加购物车模块和设置必需的属性，请执行以下步骤。

1. 创建一个名称为**购物车片段**的片段，然后向其添加一个购物车模块。
1. 向购物车模块添加一个标题。
1. 将商店选择器模块添加到购物车模块。
1. 保存片段，完成编辑，然后发布。
1. 创建一个名称为**购物车模板**的模板，然后向其添加刚才创建的购物车片段。
1. 保存模板，完成编辑，然后发布。
1. 创建一个使用新模板的页面。
1. 保存并预览页面。
1. 编辑完页面，然后发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[容器模块](add-container-module.md)

[购买框模块](add-buy-box.md)

[结帐模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)
