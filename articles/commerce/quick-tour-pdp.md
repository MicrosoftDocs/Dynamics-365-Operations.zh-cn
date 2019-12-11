---
title: 产品详细信息页概述
description: 此主题概述 Microsoft Dynamics 365 Commerce 中的产品详细信息页 (PDP)。
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
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697857"
---
# <a name="overview-of-product-details-pages"></a>产品详细信息页概述

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题概述 Microsoft Dynamics 365 Commerce 中的产品详细信息页 (PDP)。

## <a name="overview"></a>概览

PDP 提供有关产品的详细信息，可供客户用于选择产品选项，如尺寸、风格和颜色。 PDP 应展示客户要做出采购决定所需全部产品信息。

下图显示 PDP 的示例。

![产品详细信息页示例](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>标题和页脚模块

PDP 顶部是显示所有产品类别的页眉和零售商希望客户浏览的其他页面。 页面底部是页脚，其中包含可能吸引客户的各主题的快速链接。

## <a name="buy-box-module"></a>购买框模块

PDP 中最重要的模块是购买框模块。 因此，这是页面主部分中的第一项。 购买框模块是容器模块，用于承载其中包含有关产品的最重要信息的多个模块。 这些信息包括产品名称、产品图像、描述、价格和产品评分。

客户可通过购买框模块选择产品选项（例如，尺寸、风格和颜色）和将产品添加到购物车。 还可供客户在线购买产品并在商店提货。 在线购买后店内提货模块使用与 Bing 地图应用程序编程接口 (API) 之间的集成查找附近商店或客户指定的其他位置的商店。

购买框模块需要产品 ID。 此 ID 派生自页面上下文。 如果向页面上下文中不包含产品 ID 的页面添加购买框模块，则不能正确显示此信息。

## <a name="product-specifications-module"></a>产品规格模块

产品规格模块可用于展示有关产品的更多详细信息。 这些详细信息取自 Dynamics 365 Retail 中的产品属性。 产品规格模块显示其中的**可视**属性设置为 **true** 的每个属性。 它需要产品 ID 才能检索产品属性。

## <a name="recommendations-module"></a>建议模块

建议模块是 PDP 中的重要模块。 客户浏览产品时，应该会为其提供更多产品选项，以便客户找到正确的产品并进行购买。 建议可帮助客户轻松发现相关内容并继续购物。

提供了不同类型的建议列表：

- **用户也喜欢**列表基于机器学习。 它使用其他客户的交易历史记录提供建议。 此列表由建议服务生成，类似“购买了此产品的客户也购买了...”列表。 需要产品 ID 才能生成此列表。
- 可以在 Retail 中为产品配置**相关**列表。 例如，对于棕色皮质旅行手提包，可以为相关列表配置皮质或旅行用的更多手提包。 也可以在 Retail 中配置其他类型的相关列表，如**配饰**和**更多此类产品**。 需要产品 ID 才能生成此列表。 因此，如果将其添加到主页（此处页面上下文中不包含产品 ID），则此列表为空。
- 可以在 PDP 中使用算法生成的建议列表，如**热门**、**最畅销**和**新品**。 虽然这些列表与 PDP 中的产品没有直接关系，也可以用于帮助客户找到感兴趣的产品。 这些类型的列表不需要产品 ID。 它们是基于站点中的购物模式生成的一般列表。
- 编辑列表是手动精选的列表。 例如，零售商可能决定手动挑选要展示的产品的列表。

## <a name="ratings-and-reviews-module"></a>评分和评价模块

评分和评价模块显示其他客户提供的评分和评价。 还可供客户撰写自己的产品评论。 此外，其中还有一个直方图，该直方图显示产品的评分趋势。 有关详细信息，请参阅[评分和评价概述](ratings-reviews-overview.md)。

## <a name="marketing-modules"></a>市场营销模块

如果市场营销内容是特定产品的唯一内容，可将任何市场营销模块添加到 PDP。 可以通过“扩展”页面向 PDP 添加市场营销模块。 

## <a name="additional-resources"></a>其他资源

[主页概览](quick-tour-home-page.md)

[默认类别登陆页面和搜索结果页面的概述](category-search-page-overview.md)

[购物车和结帐页概述](quick-tour-cart-checkout.md)

[帐户管理页概述](quick-tour-account-management.md)
