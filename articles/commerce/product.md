---
title: 在 POS 中添加产品建议
description: 本主题介绍如何在销售点 (POS) 设备上使用产品建议。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 08784385dd1fead13f538b4e856b4bac6651a560
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969918"
---
# <a name="add-product-recommendations-on-pos"></a>在 POS 中添加产品建议

[!include [banner](includes/banner.md)]

产品建议的核心是一个革命性的业务应用程序，该应用程序适用于所有商务领域，可以带来丰富、参与度高、度身定制的产品发现体验。 若要在 POS 上实施此功能，请执行[如何向 POS 设备添加建议](add-recommendations-control-pos-screen.md)中的步骤。 

有关产品建议功能的详细信息，请参阅[产品建议概述](../commerce/product-recommendations.md)。 

## <a name="scenarios"></a>方案

将为以下 POS 方案启用产品建议。 Cloud POS 或 Modern POS (MPOS) 中支持产品建议。

1. 在 **产品详细信息** 页面中：

    - 如果售货员在查看跨不同渠道的早期交易记录时访问 **产品详细信息** 页面，建议服务将推荐更多可能搭配购买的物料。

    [![有关“产品详细信息”页的建议](./media/proddetails.png)](./media/proddetails.png)

2. 在 **交易记录** 页面中：

    - 建议引擎根据购物车中经常一起购买的物料的完整列表推荐物料。

    > [!NOTE]
    > 若要在 **交易记录** 页面中显示建议，零售商需要更新 Dynamics 365 Commerce 中的屏幕布局。 必须将 **建议** 控件拖到 **交易记录** 页面中。

    [![有关“交易记录”页的建议](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>配置 Commerce 以启用 POS 建议

要设置产品建议，请执行以下步骤：

1. 确保设备已更新为 **10.0.6 build**。
2. 按照有关如何为企业[启用产品建议](../commerce/enable-product-recommendations.md)的说明操作。
3. 可选：若要在交易记录屏幕中显示建议，请转至 **屏幕布局**，选择您的屏幕布局，启动 **屏幕布局设计器**，然后将 **建议** 控件拖到所需位置。
4. 转至 **商业参数**，选择 **机器学习**，然后在 **启用 POS 建议** 下选择 **是**。
5. 若要在 POS 中查看建议，请运行全局配置作业 **1110**。 若要体现对 POS 屏幕布局设计器所做更改，请运行渠道配置作业 **1070**。

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>排除您已启用了产品建议时遇到的问题

- 导航到 **商业参数** \> **建议列表** \> **禁用产品建议**，然后运行 **全局配置作业 \[9999\]**。 
- 如果使用 **屏幕布局设计器** 为交易记录屏幕添加了 **建议控件**，请将其一并移除。
- 如果还有其他问题，请参阅[产品建议常见问题](../commerce/faq-recommendations.md)获取详细信息。

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