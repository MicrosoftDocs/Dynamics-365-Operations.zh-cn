---
title: 购物车图标模块
description: 此主题介绍购物车图标模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9e3850d98e716d1bbea2017f6e8c9d75f19adc9
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/17/2021
ms.locfileid: "6637993"
---
# <a name="cart-icon-module"></a>购物车图标模块

[!include [banner](includes/banner.md)]

此主题介绍购物车图标模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

购物车图标模块在页面的页眉模块中提供购物车，并显示购物车中的商品数量。 将鼠标光标悬停在购物车图标上方时，购物车图标模块还会显示购物车摘要（也称为迷你购物车）。 用户不必导航到购物车页面，迷你购物车就为用户提供购物车中的商品摘要。 此外，还允许用户在对摘要满意的情况下直接转到结帐页面。 这样可以减少页面导航次数，加快结帐速度。 

下图显示了购物车图标模块的示例，该模块在 Fabrikam 标题中显示迷你购物车。

![购物车图标模块的示例。](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>模块属性

- **显示迷你购物车** – 如果为 true，此属性用于启用将鼠标光标悬停在购物车图标上方时显示的购物车摘要（迷你购物车）。 只有桌面视图端口中才支持此功能。

## <a name="module-properties-in-the-adventure-works-theme"></a>Adventure Works 主题中的模块属性

在 Adventure Works 主题中，购物车图标模块包括两个额外的迷你购物车插槽。 这些插槽作为模块定义扩展包含在内。

- **空购物车促销** – 该插槽采用内容块模块。 当购物车为空时，显示指定的内容块模块。 内容块模块可用于促销、市场营销内容和类别页面链接，以帮助客户继续他们的购物之旅。
- **促销内容** – 此插槽可用于展示促销活动，例如“订单金额超过 100 美元免运费”。 可在促销内容插槽中使用内容块、文本块和图像列表模块。

下图显示了 Adventure Works 主题中购物车图标模块的示例，该模块在迷你购物车上显示促销内容。

![Adventure Works 主题中购物车图标模块的示例](./media/AW_minicart.PNG)

> [!IMPORTANT]
> Adventure Works 主题插槽从 Dynamics 365 Commerce 版本 10.0.20 发行版本开始提供。

## <a name="add-a-cart-icon-module-to-a-page"></a>向页面添加购物车图标模块

若要添加购物车图标模块，请参阅[页眉模块](author-header-module.md)。

## <a name="additional-resources"></a>其他资源

[购物车模块](add-cart-module.md)

[结帐模块](add-checkout-module.md)

[付款模块](payment-module.md)

[收货地址模块](ship-address-module.md)

[交付选项模块](delivery-options-module.md)

[提货信息模块](pickup-info-module.md)

[订单详细信息模块](order-confirmation-module.md)

[礼品卡模块](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
