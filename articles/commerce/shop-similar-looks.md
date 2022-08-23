---
title: 启用“购买相似外观产品”建议
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中启用“购买相似外观产品”产品建议。
author: bebeale
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 26eb436d889ac81cde730daca9b44d1deeda6c74
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282042"
---
# <a name="enable-shop-similar-looks-recommendations"></a>启用“购买相似外观产品”建议

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中启用“购买相似外观产品”产品建议。

Dynamics 365 Commerce 中的“购买相似外观产品”推荐功能利用人工智能和机器学习 (AI-ML) 的力量向客户提供视觉上相似的产品建议。 通过为 Commerce 中的所有零售渠道提供“购买相似外观产品”建议，零售商可以通过帮助客户轻松找到他们想要的商品来提高客户满意度。

“购买相似外观产品”建议功能使用种子产品变型的产品图像在零售商的产品目录中查找和推荐视觉上相似的产品。 

销售点 (POS) 和电子商务体验中都提供“购买相似外观产品”建议。

### <a name="example-scenarios"></a>示例方案

- 某客户查看一件黑色条纹的毛衣，收到一条推荐类似的红色毛衣的建议。 该客户选择建议的产品而不是最初查看的产品，然后收到红色的类似产品的建议。 
- 某客户使用“购买相似外观产品”建议来发现与该客户有兴趣购买的戒指匹配的耳环。

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>在 Commerce headquarters 中启用“购买相似外观产品”建议

仅针对已将存储迁移到 Azure Data Lake Gen2 的 Commerce 用户支持产品建议。

### <a name="prerequisites"></a>先决条件

在零售商可以开始向客户显示“购买相似外观产品”建议之前，有两个先决步骤：

- 在 Commerce headquarters 中[启用产品建议](enable-product-recommendations.md)。
- 确认媒体服务器支持 HTTPS 调用。

要让建议引擎能够访问产品图像，零售商必须生成产品 URL。 要在 Commerce Headquarters 中生成产品 URL，请按照下列步骤操作。

1. 转到 **产品图像**。
1. 在操作窗格上，选择 **定义媒体模板**。
1. 在 **定义媒体模板** 属性窗格中，在 **媒体 URL** 下，选择 **生成 URL**。

> [!NOTE]
> 启用“购买相似外观产品”建议功能后，生成产品建议列表的过程将开始。 这些列表最多可能需要一天时间完成在线以及在 POS 终端上提供和显示。

要在 Commerce headquarters 中启用“购买相似外观产品”建议功能，请按照下列步骤操作。

1. 转到 **功能管理**。
1. 在可用功能列表中，搜索并选择 **购买相似外观产品**。
1. 在右窗格中，选择 **启用** 打开此服务。

下图显示了 Commerce headquarters 中 **功能管理** 页面上的 **购买相似外观产品** 功能。

![Commerce Headquarters 中“功能管理”页面上的“购买相似外观产品”功能。](./media/enableshopsimilarlooks.png)

完成上述任务后，POS 终端将自动增强，提供上下文 **购买相似外观产品** 面板。 选择 **查看更多**，POS 终端用户可以转到专用的“购买相似外观产品”页面，可以在那里进一步筛选。

> [!NOTE]
> 如果关闭“购买相似外观产品”建议功能，不会影响其他类型产品的建议。 有关产品建议的详细信息，请参阅[产品建议概述](product-recommendations.md)。

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>使用 Commerce 站点构建器将“购买相似外观产品”按钮添加到产品详细信息页面

在 Commerce headquarters 中启用“购买相似外观产品”建议功能之后，Commerce 站点构建器中的一个选项让零售商可以在任何产品详细信息页面 (PDP) 上的购买框中添加 **购买相似外观产品** 按钮。 选择此按钮的客户将被带到专用的“购买相似外观产品”页面，该页面返回外观相似的产品。 在那里，客户可以使用选择器进一步筛选产品。

要使用 Commerce 站点构建器将 **购买相似外观产品** 按钮添加到 PDP，请按照以下步骤操作。

1. 打开一个包含购买框模块的现有站点构建器页面。
1. 在左侧导航窗格中，选择购买框模块。
1. 在右侧导航窗格中，选择 **启用“购买相似外观产品”链接** 复选框。
1. 选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。 页面发布后，PDP 将包含一个 **购买相似外观产品** 按钮。

下图显示了站点构建器中示例 PDP 上的 **启用“购买相似外观产品”链接** 复选框和 **购买相似外观产品** 按钮。

![站点构建器中 PDP 上的“启用‘购买相似外观产品’链接”复选框和“购买相似外观产品”按钮。](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage](enable-adls-environment.md)

[启用产品建议](enable-product-recommendations.md)

[选择退出个性化产品建议](personalization-gdpr.md)

[在 POS 中添加产品建议](product.md)

[向交易记录屏幕添加建议](add-recommendations-control-pos-screen.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[使用演示数据创建建议](product-recommendations-demo-data.md)

[产品建议常见问题](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
