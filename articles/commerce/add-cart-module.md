---
title: 购物车模块
description: 此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696753"
---
# <a name="cart-module"></a>购物车模块

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

购物车模块是用于承载展示购物车中的项所需全部模块的容器。 例如，其中包含已添加到购物车的所有项、订单摘要和促销代码。

购物车模块基于购物车 ID 显示数据。 购物车 ID 是整个站点中可用的浏览器 cookie。

## <a name="cart-module-properties-and-slots"></a>购物车模块属性和插槽

作为容器，购物车模块控制某些基本属性，如标题和宽度。 标题通常是**购物袋**、**您的购物车**或**购物车中的项**之类文本。 宽度设置决定容器内的模块是适应该容器，还是填满屏幕。

购物车页面分为多个区域：购物车明细项、订单摘要和结帐，以及“在店内查找”功能。 每个区域映射到购物车模块中的一个插槽，而每个插槽则接受一组预定义的模块。

## <a name="modules-that-can-be-used-in-a-cart-module"></a>购物车模块中可使用的模块

- **购物车明细项** – 此模块显示已添加到购物车的每件项的摘要。 信息包括产品标题、所选维度、价格、数量和折扣。 此模块还支持“从购物车中删除”和“添加到愿望列表”等操作。 每件明细项都有一个选项，用于为项发货和从商店取项。 必须在店内提货模块中配置此选项。
- **订单摘要** – 此模块显示订单摘要。 信息包括小计、发货、税和节省。 可以为此模块配置标题。
- **促销代码** – 客户可使用此模块兑换促销代码。 可以应用或删除促销代码。
- **结帐** – 此模块发起结帐操作，并将用户重定向到结帐页。 必须为此模块配置三个链接：

    - **结帐** – 如果客户尚未登录，此链接将强制客户登录。
    - **来宾结帐** – 此链接用于供匿名客户下订单。 仅当客户未登录时才显示。
    - **返回购物** – 此链接用于供客户转到主页或其他任何页，以便继续购物。

- **内容丰富块** – 此模块支持购物车模块中的自定义消息。 消息由内容管理系统 (CMS) 驱动。 可以添加任何消息，如“订单问题请致电 1-800-Fabrikam”。
- **在商店中提货** – 此模块显示附近可提货的商店的列表。 默认情况下，此模块显示客户位置半径 50 英里内的商店。 但是，可以在模块中自定义搜索半径。 如果开启了库存检查功能，并且显示了相应的现货或库存不足消息，则可对每家商店执行库存检查。
- **通过 Bing 地图搜索商店** – 可在店内提货模块中使用此模块。 可供客户通过输入位置搜索商店。 Bing 地图地理编码应用程序编程接口 (API) 用于将客户输入的位置转换为维度和经度。 如果不使用此模块，则仅显示客户当前位置附近的商店，客户不能搜索其他位置。

## <a name="cart-module-settings"></a>购物车模块设置

购物车模块中有三个可配置的设置：

- **最大数量** – 可以添加到购物车的每种项的最大数量。 例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。
- **库存检查** – 如果此值设置为 **True**，则只有在购买框模块确信某种项有现货时，才能将此项添加到购物车中。 将在项发货时和在商店中提货时执行库存检查。 如果此值设置为 **False**，则向购物车添加项和下订单前，不进行库存检查。
- **库存缓冲区** – 库存实时维护，如果多位客户下订单，则很难维持精确的库存计数。 因此，可以为库存定义缓冲区。 进行库存检查时，如果库存比缓冲区数量少，则将产品视为库存不足。 因此，当通过多个渠道快速进行销售，导致库存计数无法充分同步时，出售库存不足的项的风险较低。

## <a name="retail-server-interaction"></a>Retail Server 交互

购物车模块使用 Retail Server API 检索产品信息。 浏览器 cookie 中的购物车 ID 用于从 Retail Server 检索所有产品信息。

## <a name="add-a-cart-module-to-a-page"></a>向页面添加购物车模块

若要向新页面添加购物车模块和设置必需的属性，请执行以下步骤。

1. 创建一个名称为**购物车片段**的片段，然后向其添加一个购物车模块。
1. 在购物车模块的**购物车明细项**插槽中，添加购物车明细项模块。
1. 在**订单摘要**插槽中，添加一个订单摘要模块。
1. 在**促销代码**插槽中，添加一个促销代码模块。
1. 在**结帐**插槽中，添加一个结帐模块。
1. 在**在店内查找**插槽中，添加一个店内提货模块。
1. 在店内提货模块内的插槽中，选择**商店搜索**插槽，然后添加一个通过 Bing 地图搜索商店模块。
1. 签入片段，然后发布。
1. 创建一个名称为**购物车模板**的模板，然后向其添加刚才创建的购物车片段。
1. 保存模板，签入，然后发布。
1. 创建一个使用新模板的页面。
1. 保存并预览页面。
1. 签入页面，然后发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[容器模块](add-container-module.md)

[购买框模块](add-buy-box.md)

[结帐模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)
