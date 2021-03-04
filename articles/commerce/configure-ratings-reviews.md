---
title: 配置评分和评价
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置电子商务站点以显示客户评分和评价。
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edd2082b5d2cafcb955f8e3c7762bcba523ac479
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410388"
---
# <a name="configure-ratings-and-reviews"></a>配置评分和评价

[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置电子商务站点以显示客户评分和评价。

## <a name="overview"></a>概览

电子商务网站中的评分和评价可帮助客户在做出采购决定之前了解产品，方法是对其显示其他客户对这些产品的看法。 对于电子商务网站，评分和评价也是用于收集有关产品的客户反馈的机制。 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>配置站点以显示评分和评价

评分或评价的配置值（如租户 ID、评论文本长度和评论标题长度）在站点级别配置。 

若要配置站点以显示评分或评价，请执行以下步骤。 

1. 转到 **主 \> 站点**。
1. 选择站点的名称。 
1. 转到 **站点设置 \> 扩展**。 
1. 在 **评论文本最大长度** 字段中，输入评论文本可包含的最大字符数（例如，**1000**）。 
1. 在 **评论标题最大长度** 字段中，输入评论标题可包含的最大字符数（例如，**55**）。 
1. 选择 **保存并发布**。 

下图显示此配置在 Dynamics 365 Commerce 中的显示效果。

![配置站点以显示评分和评价](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>将产品评分链接到 PDP 的“评论”部分

将在 PDP 顶部的产品标题下显示产品评分。 可将产品评分配置为链接到同一个 PDP 的 **评论** 部分。 

若要将产品评分链接到 PDP 的 **评论** 部分，请执行以下步骤。

1. 打开 PDP 模板。 
1. 转到 **购买框容器模块设置**。
1. 在 **购买框** 下，选择 **产品评分**，然后选中 **链接单击以显示完整评论模块** 复选框。

下图显示此配置在 Dynamics 365 Commerce 中的显示效果。

![将产品评分链接到 PDP 的“评论”部分](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>配置隐私和政策页的链接

若要配置隐私和政策页的链接，请执行以下步骤。

1. 转到 **主 \> 站点**。
1. 选择站点的名称。 
1. 转到 **站点设置 \> 扩展**。
1. 在 **路由** 选项卡中 **RNR 隐私和政策** 下，选择 **添加链接**。 如果已经输入了链接，但希望将其替换，请选择该链接。 
1. 在 **添加链接** 对话框中，选择隐私和政策页的链接，然后选择 **确定**。 
1. 选择 **保存并发布**。 

下图显示此配置在 Dynamics 365 Commerce 中的显示效果。

![配置隐私和政策页的链接](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>配置产品详细信息页中的评分和评论模块

有关配置产品详细信息页中的评分和评论模块的信息，请参阅[评分和评论模块](ratings-reviews-modules.md)。

## <a name="additional-resources"></a>其他资源

[评分和评价概览](ratings-reviews-overview.md)

[选择使用评分和评价](opt-in-ratings-reviews.md)

[管理评分和评价](manage-reviews.md)

[配置产品详细信息页中的评分和评论模块](ratings-reviews-modules.md)

[在 Dynamics 365 Retail 中同步产品评分](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]