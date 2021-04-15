---
title: 产品建议概览
description: 本主题提供有关产品建议的一般信息。 客户可通过产品建议轻松、快速地找到所需产品，甚至找到最初不打算购买的产品。
author: Moonma
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 044a5c21e4ebf1bf83edc74335e655b9388bc1d4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795589"
---
# <a name="product-recommendations-overview"></a>产品建议概览

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce 可用于在电子商务网站和销售点 (POS) 设备上显示产品建议。 产品建议是客户可能感兴趣的项。 建议基于其他客户在在线商店和实体商店中的购买趋势。

客户可通过产品建议轻松、快速地找到所需产品，同时享受良好的服务体验。 甚至可使用交叉销售和向上销售帮助客户找到甚至最初不打算购买的更多产品。 使用建议增强产品发现时，可以产生更多转化商机，帮助提高销售利润，甚至帮助加强客户满意度和保留。

在电子商务中，Microsoft Recommendations 机器学习技术大幅助力产品建议。

## <a name="recommendation-service"></a>建议服务

产品建议服务按照以下方式使用人工智能和机器学习 (AI-ML) 技术：

- 从 Commerce 操作数据库提取建议服务所需格式的数据并发送到 Azure Data Lake Storage 或实体商店。
- 建议服务使用存储的数据培训 **用户也喜欢**、**人气组合**、**新品**、**最畅销** 和 **热门** 列表的建议模型。

## <a name="scenarios"></a>方案

以下方案支持产品建议：

- **在电子商务中用于浏览或登录页面的任何商店页面上：** 如果客户或商店助理访问某个商店页面，建议引擎可在 **新品**、**最畅销** 和 **热门** 列表中推荐产品。
- **在“产品详细信息”页中：** 如果客户或商店助理访问 **产品详细信息** 页，建议引擎将推荐也可能购买的更多商品。 这些商品在 **用户也喜欢** 列表中显示。
- **在“交易记录”页或结帐页中：** 建议引擎基于购物篮中的完整商品列表推荐商品。 这些商品在 **人气组合** 列表中显示。
- **个性化建议：** 商品交易商可以为登录客户提供个性化的 **为您推荐** 列表，以及新功能，从而允许根据该客户对现有列表方案进行个性化设置。 若要了解详细信息，请参阅[启用个性化建议](personalized-recommendations.md)。

### <a name="types-of-product-recommendations"></a>产品建议的类型

下表介绍可供零售商在其 Dynamics 365 Commerce 解决方案中通过[产品收集模块](product-collection-module-overview.md)实施的各种自动化产品建议。 零售商还可以为登录用户显示个性化结果（如果站点作者选择该选项）。

| 产品集合模块  | 类型 | 说明 |
|----------------------------|------|-------------|
| 全新                        | 算法 | 此模块显示最近已经分类为渠道和目录的最新产品的列表。 |
| 最畅销               | 算法 | 此模块显示按销售数最高排名的产品的列表。 |
| 热门                   | 算法 | 此模块显示给定期间表现最出色的产品的列表，并按最高销售数排名。  |
| 经常搭配购买的产品 | AI-ML | 此模块推荐通常与客户的当前购物车内容一起购买的产品的列表。 |
| 人们还喜欢           | AI-ML | 此模块根据消费者购物模式为给定种子产品推荐产品。 |
| 为您推荐              | AI-ML | 此模块根据已登录用户的购买模式推荐个性化的产品列表。 对于来宾用户，此列表将被折叠。 |

## <a name="additional-resources"></a>其他资源

[在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage](enable-adls-environment.md)

[启用产品建议](enable-product-recommendations.md)

[启用个性化建议](personalized-recommendations.md)

[选择退出个性化产品建议](personalization-gdpr.md)

[启用“购买类似外观”建议](shop-similar-looks.md)

[在 POS 上添加产品建议](product.md)

[向交易记录屏幕添加建议](add-recommendations-control-pos-screen.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[使用演示数据创建建议](product-recommendations-demo-data.md)

[产品建议常见问题](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]