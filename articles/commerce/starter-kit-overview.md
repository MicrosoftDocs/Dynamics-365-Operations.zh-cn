---
title: 模块库概览
description: 本文概述 Microsoft Dynamics 365 Commerce 模块库。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d9dc07b3f6417c7e284c6555c2818c2a782d7683
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268938"
---
# <a name="module-library-overview"></a>模块库概览

[!include [banner](includes/banner.md)]

本文概述 Microsoft Dynamics 365 Commerce 模块库。

Dynamics 365 Commerce 模块库是可用于生成电子商务网站的模块的集合。 模块同时采用用户界面 (UI) 和功能行为。

可将主题应用于模块库中的模块以更改其外观。 这些主题使用级联样式表 (CSS)。 模块库中提供一个名称为“Fabrikam”的虚构电子商务站点主题，可将其用作参考。

## <a name="module-library-modules"></a>模块库模块

模块库中提供以下类型的模块：

- **容器模块** – 容器模块是充当其他模块的主机的简单模块。 用于控制模块在其内的布局。
- **市场营销模块** – 市场营销模块包括内容块、文本块、视频播放器和传送模块。 所有这些模块都可用于展示内容。 可以放到任何页面中，并由内容管理系统 (CMS) 的数据驱动。
- **页眉和页脚模块** – 页眉和页脚模块在所有站点页的页眉和页脚中显示。 可以根据需要通过属性配置这些模块。
- **搜索模块** –可以使用页眉中的搜索模块发现产品。 搜索结果在搜索结果页中显示。 也可以在类别页中发现产品，类别页是渠道导航层次结构中支持的每个类别的专用页。 此外，还可以使用优化器模块进一步筛选搜索结果和类别页中的结果。
- **产品详细信息页模块** – 产品详细信息页使用多个模块显示产品信息。 客户可使用购买框模块查看产品和将产品添加到购物车。 其他模块（如技术规范模块）显示产品详细信息。 评分和评价模块可用于查看和提供评价。
- **在线购买，店内提货模块** – 在线购买，店内提货模块与 Bing 地图集成。 可用于查找客户可提取已购买产品的附近商店。
- **购买模块** – 购买模块中包含购物车模块，后者可用于将商品添加到购物车。 结帐模块捕获装运地址、交货选项和礼品卡、会员计划与信用卡信息，以便处理订单。 下订单之后，可使用订单确认模块显示确认详细信息。
- **帐户管理模块** – 客户可使用登录模块登录到现有帐户，可使用注册模块创建新帐户。 创建帐户之后，可使用订单历史记录模块查看最近订单，可使用订单详细信息模块查看订单详细信息。
- **建议模块** – 可使用产品放置模块显示建议。 此模块支持算法列表和编辑列表，这些列表可在任何页面中展示。

## <a name="additional-resources"></a>其他资源

[容器模块](add-container-module.md)

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
