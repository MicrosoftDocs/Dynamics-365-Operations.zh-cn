---
title: 页眉模块
description: 此主题介绍页眉模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885470"
---
# <a name="header-module"></a>标题模块

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题介绍页眉模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。

## <a name="overview"></a>概览

页眉模块是用于承载页面页眉中将显示的所有模块的特殊容器。 例如，可以包括您的站点徽标、导航层次结构的链接、站点中其他页面的链接，以及搜索栏。

针对正在用于查看站点的设备（即台式机设备或移动设备）自动优化了页眉模块。 例如，在移动设备上，导航栏折叠为**菜单**按钮（有时称为*汉堡包按钮*）。

## <a name="properties-of-a-header"></a>页眉的属性

与一般容器一样，页眉模块支持**标题**和**宽度**属性。

页眉模块有多个插槽。 例如，有参考消息、导航菜单、徽标、搜索栏、购物车图标、愿望列表图标和帐户信息的插槽。 每个插槽支持一组特定模块。

## <a name="modules-that-are-available-in-a-header-module"></a>页眉模块中的可用模块

页眉模块中可使用以下模块：

- **导航菜单** – 导航菜单提供渠道导航层次结构和其他静态导航链接。 可以在 Dynamics 365 Retail 中配置渠道导航层次结构。 配置的项然后显示为页眉导航。 此外，可配置静态导航链接，也可以提供电子商务站点中的其他页面的相对链接。 可以靠左、靠右或居中对齐页眉本身。
- **购物车图标** – 购物车图标是表示购物车的特殊图标。 其在页眉中显示，指示购物车中的项数。 购物车页面的链接应该伴有购物车图标，所以当客户与该图标交互时，可以将客户重定向到购物车页。
- **愿望列表图标** – 愿望列表图标在页眉中显示，用于指示已向客户的愿望列表添加的项数。 愿望列表页面的链接应该伴有此图标，所以当客户与该图标交互时，可以将客户重定向到愿望列表页。
- **登录模块** – 登录模块在页眉中显示。 用于供客户登录其帐户或注册帐户。 如果客户已登录，可将模块配置为显示帐户页、订单历史记录页或其他页的链接。
- **徽标模块** – 此模块显示用于表示零售商和品牌的徽标。 这是具有链接的图像。 通常将此链接配置为具有到主页的重定向。因此，客户可从站点的任何页面快速回到主页。
- **预警** – 预警在页眉中显示，用于显示为站点中的所有页面应用的内联消息。 例如，一个预警可能显示消息“年度促销将于 2 天后结束”。
- **搜索栏** – 用户可使用搜索栏输入搜索词，以便搜索产品。 必须为模块配置搜索结果页的 URL。 可配置查询字符串参数（默认值为 **"q"**）。 搜索栏有一个自动建议插槽，应该在其中添加自动建议模块。
- **自动建议** – 自动建议模块显示自动建议的结果。 这些结果可以是可以在其中找到搜索词的关键字、产品或类别。

## <a name="create-a-header-module"></a>创建标题模块

若要创建页眉模块，请执行以下步骤。

1. 创建其中包含页眉模块的页面片段。
1. 向页眉模块中的插槽添加模块。
1. 更新每个模块的设置。
1. 保存页面片段。 
1. 签入页面，然后发布。

若要帮助确保每个页面中显示页眉，请在为站点创建的每个页面模板中执行以下步骤。

1. 在默认页面中，向主插槽中的页眉添加其中包含页眉模块的页面片段。
1. 保存模板。 
1. 签入模板，然后发布。

## <a name="additional-resources"></a>其他资源

[入门套件概览](starter-kit-overview.md)

[容器模块](add-container-module.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)
