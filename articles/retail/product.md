---
title: POS 中的产品建议
description: 本主题介绍如何在销售点 (POS) 设备上使用产品建议。
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c78fc1f2f1bb08d01828a8b71ad5d3c16ad31b86
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278364"
---
# <a name="product-recommendations-on-pos"></a>POS 中的产品建议

[!include [banner](includes/banner.md)]

产品建议的核心是一个革命性的业务应用程序，该应用程序适用于所有零售领域，可以带来丰富、参与度高、度身定制的产品发现体验。 若要在 POS 上实施此功能，请执行[如何向 POS 设备添加建议](add-recommendations-control-pos-screen.md)中的步骤。 

有关产品建议功能的详细信息，请参阅[产品建议概述](../commerce/product-recommendations.md)。 

## <a name="scenarios"></a>方案

将为以下 POS 方案启用产品建议。 Cloud POS 或 Modern POS (MPOS) 中支持产品建议。

1. 在**产品详细信息**页面中：

    - • 如果售货员在查看跨不同渠道的早期交易记录时访问**产品详细信息**页面，建议服务将推荐更多可能搭配购买的物料。

    [![有关“产品详细信息”页的建议](./media/proddetails.png)](./media/proddetails.png)

2. 在**交易记录**页面中：

    - • 建议引擎根据购物车中经常一起购买的物料的完整列表推荐物料。

    > [!NOTE]
    > 若要在**交易记录**页面中显示建议，零售商需要更新 Dynamics 365 for Retail 中的屏幕布局。 必须将**建议**控件拖到**交易记录**页面中。

    [![有关“交易记录”页的建议](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a>配置 Dynamics 365 Retail 以启用 POS 建议

要设置产品建议，请执行以下步骤：

1. 确保设备已更新为 **10.0.6 build**。
2. 按照有关如何为企业[启用产品建议](../commerce/enable-product-recommendations.md)的说明操作。
3. 可选：若要在交易记录屏幕中显示建议，请转至**屏幕布局**，选择您的屏幕布局，启动**屏幕布局设计器**，然后将**建议**控件拖到所需位置。
4. 转至**零售参数**，选择**机器学习**，然后在**启用 POS 建议**下选择**是**。
5. 若要在 POS 中查看建议，请运行全局配置作业 **1110**。 若要体现对 POS 屏幕布局设计器所做更改，请运行渠道配置作业 **1070**。



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>排除您已启用了产品建议时遇到的问题

- 导航到**零售参数** \> **建议列表** \> **禁用产品建议**，然后**运行全局配置 \[9999\]**。 
- 如果使用**屏幕布局设计器**为交易记录屏幕添加了**建议控件**，请将其一并移除。
- 如果还有其他问题，请参阅[建议常见问题](../commerce/faq-recommendations.md)获取详细信息。

## <a name="additional-resources"></a>其他资源

[向 POS 设备上的交易记录页添加建议控件](add-recommendations-control-pos-screen.md)
[产品建议概述](../commerce/product-recommendations.md)
[启用产品建议](../commerce/enable-product-recommendations.md) 
