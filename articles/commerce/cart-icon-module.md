---
title: 购物车图标模块
description: 此主题介绍购物车图标模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6771a84118504cd5c8e44302380eb970e4658902
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411081"
---
# <a name="cart-icon-module"></a>购物车图标模块

[!include [banner](includes/banner.md)]

此主题介绍购物车图标模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。

## <a name="overview"></a>概览

购物车图标模块在页面的页眉模块中提供购物车，并显示购物车中的商品数量。 将鼠标光标悬停在购物车图标上方时，购物车图标模块还会显示购物车摘要（也称为迷你购物车）。 用户不必导航到购物车页面，迷你购物车就为用户提供购物车中的商品摘要。 此外，还允许用户在对摘要满意的情况下直接转到结帐页面。 这样可以减少页面导航次数，加快结帐速度。 

下图显示了购物车图标模块的示例，该模块在 Fabrikam 标题中显示迷你购物车。

![购物车图标模块的示例](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>模块属性

- **显示迷你购物车** – 如果为 true，此属性用于启用将鼠标光标悬停在购物车图标上方时显示的购物车摘要（迷你购物车）。 只有桌面视图端口中才支持此功能。


## <a name="add-a-cart-icon-module-to-a-page"></a>向页面添加购物车图标模块

若要添加购物车图标模块，请参阅[页眉模块](author-header-module.md)。


## <a name="additional-resources"></a>其他资源

[购买框模块](add-buy-box.md)

[购物车模块](add-cart-module.md)

[结账模块](add-checkout-module.md)

[订单确认模块](order-confirmation-module.md)

[页眉模块](author-header-module.md)

[页脚模块](author-footer-module.md)
