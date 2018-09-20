---
title: "个性化产品建议"
description: "此主题提供可以在销售点 (POS) 设备上显示的 Dynamics 365 for Retail 产品建议的信息。"
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: 7925a37c595f5ffa040747462d3ea60a3da41858
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2018

---

# <a name="personalized-product-recommendations"></a>个性化产品建议

[!include [banner](includes/banner.md)]

> [!NOTE]
> 我们将移除当前的产品建议服务版本，因为我们为这项功能重新设计了更出色的算法和更新的面向零售的功能。 有关详细信息，请参阅[已删除或弃用的功能](../dev-itpro/migration-upgrade/deprecated-features.md)。 

在 Dynamics 365 for Retail 中，可在销售点 (POS) 设备中显示产品建议。 建议是客户可能根据其购买历史记录感兴趣的商品、其愿望列表中的商品，以及其他客户在线商店和实体商店购买的商品。 对于目录丰富的零售商，建议可以帮助客户发现产品。 通过展示针对客户兴趣和购买习惯的产品，产品建议可以帮助零售商开展追加销售和交叉销售，以及增强客户的凝聚力。 在 Dynamics 365 for Retail 中，认知服务和 Microsoft Azure 机器学习为产品建议提供支持。


<a name="scenarios"></a>方案
---------

将为以下 POS 方案启用产品建议。 Cloud POS 或 Modern POS (MPOS) 中支持产品建议。

1.  在**产品详细信息**页面中：

-   如果售货员在查看跨不同渠道的早期交易记录时访问**产品详细信息**页面，建议引擎将推荐更多可能搭配购买的物料。
-   如果售货员将客户添加到交易记录，然后访问**产品详细信息**页面，建议引擎将使用该客户的交易记录历史信息提供个性化建议。

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  在**交易记录**页面中：

-   建议引擎根据购物篮中的整个物料列表推荐物料。
-   如果售货员将客户添加到交易记录，建议引擎将使用该客户的交易记录历史信息和购物篮中的物料列表提供个人建议。

> [!NOTE]
> 若要在**交易记录**页面中显示建议，零售商需要更新 Dynamics 365 for Retail 中的屏幕布局。 必须将**建议**控件拖到**交易记录**页面中。 [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  在**客户详细信息**页面中：
    -   建议引擎根据客户愿望列表中的用户 ID 和物料推荐物料。

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>配置 Dynamics 365 for Retail 以启用 POS 建议
若要设置产品建议，需要执行以下操作。

1.  确保已选择了正确的**法人**。
2.  导航到**实体商店**，选择**零售销售**，然后单击**刷新**。 这将使用您的操作数据库的演示数据（或您的数据），并会将其移至实体商店。
3.  可选：若要在交易记录屏幕中显示建议，请转至**屏幕布局**，选择您的屏幕布局，启动**屏幕布局设计器**，然后将**建议**控件拖到所需位置。

4.  转至**零售参数**，选择**机器学习**，然后在**启用 POS 建议**下选择**是**。
5.  若要在 POS 中查看建议，请运行全局配置作业 **1110**。 若要体现对 POS 屏幕布局设计器所做更改，请运行渠道配置作业 **1070**。

## <a name="how-does-it-work"></a>工作原理
刷新**实体商店**实体时，将执行以下操作。

-   从 Dynamics 365 for Retail 操作数据库提取认知服务所需格式的数据并发送到实体商店。
-   Azure Data Factory (ADF) 使用这些数据清理将 Hive 脚本用作ADF 活动一部分的数据。 清理的数据存储在 blob 存储中。
-   认知服务 API 使用 blob 存储中的数据训练建议模型。

开启**启用建议**并运行配置作业时，将执行以下操作。

-   从该 API 选取模型凭据和 ID 并存储到 Dynamics 365 for Retail 操作数据库、AOS 的 web.config 和零售服务器中。
-   将模型凭据和 ID 提供给 CRT，以便可以处理联机模式下对 Cloud POS 和 MPOS 的产品建议的请求。

> ## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>排除您已启用了产品建议时遇到的问题 
> - 导航到**零售参数** > **机器学习** > **禁用产品建议**，然后运行**全局配置 [1110]**。 如果找不到**机器学习**选项卡，请联系 Dynamics 支持。 
> 
> - 如果使用**屏幕布局设计器**为交易记录屏幕添加了**建议控件**，请将其一并移除。 



<a name="additional-resources"></a>其他资源
--------

[向 POS 设备上的交易记录页添加建议控件](add-recommendations-control-pos-screen.md)




