---
title: 产品建议概览
description: 本主题提供有关产品建议的一般信息。 客户可通过产品建议轻松、快速地找到所需产品，甚至找到最初不打算购买的产品。
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024971"
---
# <a name="product-recommendations-overview"></a>产品建议概览

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce 可用于在电子商务网站和销售点 (POS) 设备上显示产品建议。 产品建议是客户可能感兴趣的项。 建议基于其他客户在在线商店和实体商店中的购买趋势。

客户可通过产品建议轻松、快速地找到所需产品，同时享受良好的服务体验。 甚至可使用交叉销售和向上销售帮助客户找到甚至最初不打算购买的更多产品。 使用建议帮助发现产品时，可以产生更多转化商机，帮助提高销售利润，甚至帮助加强客户满意度和保留。

在 Commerce 中，Microsoft Recommendations 机器学习技术大幅助力产品建议。


## <a name="scenarios"></a>方案

以下方案支持产品建议：

- **在电子商务中用于浏览或登录页面的任何商店页面上：** 如果客户或商店助理访问某个商店页面，建议引擎可在**新品**、**最畅销**和**热门**列表中推荐产品。
- **在“产品详细信息”页中：** 如果客户或商店助理访问**产品详细信息**页，建议引擎将推荐也可能购买的更多商品。 这些商品在**用户也喜欢**列表中显示。
- **在“交易记录”页或结帐页中：** 建议引擎基于购物篮中的完整商品列表推荐商品。 这些商品在**人气组合**列表中显示。
- **个性化建议：** 商品交易商可以为登录客户提供个性化的**为您推荐**列表，以及新功能，从而允许根据该客户对现有列表方案进行个性化设置。 要了解更多信息，请参阅功能文档：[启用个性化建议。](personalized-recommendations.md)

## <a name="recommendation-service"></a>建议服务

产品建议按照以下方式使用建议机器学习技术：

- 从 Commerce 操作数据库提取建议服务所需格式的数据并发送到实体商店。
- 建议服务使用这些数据培训**用户也喜欢**、**人气组合**、**新品**、**最畅销**和**热门**列表的建议模型。

## <a name="additional-resources"></a>其他资源

[启用产品建议](enable-product-recommendations.md)

[启用个性化建议](personalized-recommendations.md)

[产品集合模块概览](product-collection-module-overview.md)

[创建策划的产品建议列表](create-editorial-recommendation-lists.md)

[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)

[向页面添加建议列表](add-reco-list-to-page.md)
