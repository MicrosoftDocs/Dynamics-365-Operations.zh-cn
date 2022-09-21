---
title: 在 POS 中添加产品建议
description: 本文介绍如何在销售点 (POS) 设备上使用产品建议。
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460048"
---
# <a name="add-product-recommendations-on-pos"></a>在 POS 中添加产品建议

[!include [banner](includes/banner.md)]

产品建议的核心是一个革命性的业务应用程序，该应用程序适用于所有商务领域，可以带来丰富、参与度高、度身定制的产品发现体验。 若要在 POS 上实施此功能，请执行[如何向 POS 设备添加建议](add-recommendations-control-pos-screen.md)中的步骤。 

有关产品建议功能的详细信息，请参阅[产品建议概述](../commerce/product-recommendations.md)。 

## <a name="scenarios"></a>方案

将为以下 POS 方案启用产品建议。 Cloud POS 或 Modern POS (MPOS) 中支持产品建议。

1. 在 **产品详细信息** 页面中：

    - 如果售货员在查看跨不同渠道的早期交易记录时访问 **产品详细信息** 页面，建议服务将推荐更多可能搭配购买的物料。 根据服务的附加产品，零售商可以显示产品的 **购买相似外观产品** 和 **购买相似说明产品** 建议，以及针对以前购买过的用户的个性化建议。

    [![有关“产品详细信息”页面的建议。](./media/proddetails.png)](./media/proddetails.png)

2. 在 **交易记录** 页面中：

    - 建议引擎根据购物车中经常一起购买的物料的完整列表推荐物料。

    > [!NOTE]
    > 若要在 **交易记录** 页面中显示建议，零售商需要更新 Dynamics 365 Commerce 中的屏幕布局。 必须将 **建议** 控件拖到 **交易记录** 页面中。

    [![有关“交易”页面的建议。](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>配置 Commerce 以启用 POS 建议 

要设置产品建议，确认您已按照[启用产品建议](../commerce/enable-product-recommendations.md)中的步骤完成 Commerce 产品建议的预配过程。 默认情况下，在您完成预配步骤并且数据已成功修改后，建议会同时显示在 **产品详细信息** 页面和 **客户详细信息** 页面。 

## <a name="add-recommendations-to-the-transaction-screen"></a>向交易记录屏幕添加建议

1. 要向交易屏幕添加建议，请按照[向交易屏幕添加建议](add-recommendations-control-pos-screen.md)中的步骤操作。
1. 要反映在 POS 屏幕布局设计器中所做的更改，在 Commerce headquarters 中运行渠道配置作业 **1070**。

> [!NOTE] 
> 如果要使用 RecoMock 逗号分隔值 (CSV) 文件启用 POS 建议，您必须在配置布局管理器之前将 CSV 文件部署到 Microsoft Dynamics Lifecycle Services (LCS) 资产库。 如果您使用 RecoMock CSV 文件，则不必启用建议。 CSV 文件仅用于演示目的。 建议希望模拟建议列表外观以用于演示目的而无需购买附加产品库存单位 (SKU) 的客户或解决方案架构师使用。

## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage](enable-adls-environment.md)

[启用产品建议](enable-product-recommendations.md)

[启用个性化建议](personalized-recommendations.md)

[选择退出个性化产品建议](personalization-gdpr.md)

[启用“购买类似外观”建议](shop-similar-looks.md)

[向交易记录屏幕添加建议](add-recommendations-control-pos-screen.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[使用演示数据创建建议](product-recommendations-demo-data.md)

[产品建议常见问题](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
