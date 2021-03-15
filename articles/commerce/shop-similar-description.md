---
title: 启用“购买相似说明产品”建议
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中启用“购买相似说明产品”产品建议。
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b3b7abf47a3bdacaa4b91ae32b68a809a84b0b1d
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098614"
---
# <a name="enable-shop-similar-description-recommendations"></a>启用“购买相似说明产品”建议

[!include [banner](includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 中启用“购买相似说明产品”产品建议。

Dynamics 365 Commerce 中的“购买相似说明产品”推荐功能利用人工智能和机器学习 (AI-ML) 提供说明与客户正在查找的产品相似的产品建议。 通过为 Commerce 中的所有零售渠道提供“购买相似说明产品”建议，零售商可以帮助客户轻松找到他们想要的商品。

“购买相似说明产品”建议功能使用种子产品的产品名称和说明在零售商的产品目录中查找和推荐相似产品。

销售点 (POS) 和电子商务体验中都提供“购买相似说明产品”建议。

## <a name="example-scenarios"></a>示例方案

下面的示例场景说明了“购买相似说明产品”功能可以提供的建议类型：

- 客户查看一副复古风的角质架眼镜，然后收到了基于零售商行业上下文的其他设计相似的眼镜的建议。
- 客户使用“购买相似说明产品”建议来发现与他们先前从零售商处购买的咖啡口味相似的咖啡口味。

## <a name="set-up-shop-similar-description-recommendations"></a>设置“购买相似说明产品”建议

仅针对已将存储迁移到 Azure Data Lake Storage Gen2 的 Commerce 用户支持产品建议。

### <a name="prerequisites"></a>先决条件

您必须完成以下先决条件，然后才能够向客户显示“购买相似说明产品”建议：

- 在 Commerce headquarters 中[启用产品建议](enable-product-recommendations.md)。
- 确认媒体服务器支持 HTTPS 调用。

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>启用“购买相似说明产品”建议功能

要在 Commerce headquarters 中启用“购买相似说明产品”建议功能，请按照下列步骤操作。

1. 在 **功能管理** 工作区中，在可用功能列表中，搜索并选择 **购买相似说明产品**。
1. 从右窗格中，选择 **启用**。

> [!NOTE]
> 启用此功能时，系统将开始生成产品建议列表。 这些列表最多可能需要一天时间来在线和在 POS 终端上提供和显示。
>
> 如果关闭此功能，其他类型的产品建议不会受到影响。 有关产品建议的详细信息，请参阅[产品建议概述](product-recommendations.md)。

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>在产品详细信息页上添加“购买相似说明产品”按钮

在 Commerce headquarters 中启用“购买相似说明产品”建议功能之后，您可以在任何产品详细信息页 (PDP) 上的购买框中添加 **购买相似说明产品** 按钮。 选择此按钮的客户将被带到专用的 **购买相似说明产品** 页面，该页面显示相似的产品。 然后，客户可以使用选择器进一步筛选产品。

要使用 Commerce 站点构建器将 **购买相似说明产品** 按钮添加到 PDP，请按照以下步骤操作。

1. 打开一个包含购买框模块的现有站点构建器页面。
1. 在左侧导航窗格中，选择购买框模块。
1. 在右侧窗格中，选择 **启用“购买相似说明产品”链接** 复选框。
1. 选择 **保存**。
1. 选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。 页面发布后，PDP 将包含一个 **购买相似说明产品** 按钮。

下图显示了站点构建器中示例 PDP 上的 **启用“购买相似说明产品”链接** 复选框和 **购买相似说明产品** 按钮。

![站点构建器中 PDP 上的“启用‘购买相似说明产品’链接”复选框和“购买相似说明产品”按钮](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage](enable-adls-environment.md)

[启用产品建议](enable-product-recommendations.md)

[启用“购买相似外观产品”建议](shop-similar-looks.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[产品建议常见问题](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]