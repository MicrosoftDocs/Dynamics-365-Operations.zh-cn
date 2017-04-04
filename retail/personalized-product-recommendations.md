---
title: Personalized product recommendations overview
description: "在工序的 Dynamics 365，产品建议可以{{正要：on_the_point_of}}销售点 (POS) 设备的时间将显示。 建议物料是基于的采购历史记录、为感物料兴趣其利息和物料可以是客户购买的客户其他在线和在砖和泥商店。 对于使用高目录，则帮助零售商的产品具有查看的客户。 展示通过产品所针对的客户的利息和采购习惯产品，建议以帮助销售和促销零售商的交互，并且可以提高客户保留。 在工序的 Dynamics 365，产品建议为 powered by 认知服务和 Microsoft Azure 机器学习。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Personalized product recommendations overview

在工序的 Dynamics 365，产品建议可以{{正要：on_the_point_of}}销售点 (POS) 设备的时间将显示。 建议物料是基于的采购历史记录、为感物料兴趣其利息和物料可以是客户购买的客户其他在线和在砖和泥商店。 对于使用高目录，则帮助零售商的产品具有查看的客户。 展示通过产品所针对的客户的利息和采购习惯产品，建议以帮助销售和促销零售商的交互，并且可以提高客户保留。 在工序的 Dynamics 365，产品建议为 powered by 认知服务和 Microsoft Azure 机器学习。

<a name="scenarios"></a>方案
---------

产品以下方案的 POS 启用建议。 它们可用于云 POS 或 Modern POS (MPOS)。

1.  **在产品**详细信息"页面上：

-   如果商店关联。**访问产品**详细信息"页面上，查看在跨不同的渠道的以前的交易记录，则建议引擎。可以将采购的其他物料时。
-   如果商店关联客户添加到交易记录。**然后访问产品详细信息**页，使用客户的交易历史记录，建议引擎提供个性化的建议。

[] (![proddetails。/media/proddetails.png)](。/media/proddetails.png)

1.  ** **在交易记录页：

-   建议基于建议引擎物料整个列表的物料。的购物车。
-   如果商店关联客户添加到交易记录中，则使用物料和客户的交易记录的列表。篮，建议的引擎提供个人建议。

**注释**查看有关建议** **的交易记录页，该零售商需要更新在 Dynamics 365 的屏幕布局操作。 **必须删除建议**控件。** **交易记录页。 [] (![transactionscreenmultipleproductslargemessengersbag-5。/media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](。/media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

1.  ** **在客户详细信息"页面上：
    -   建议引擎建议为基于在客户端中的用户 ID 的物料和物料。

[] (![customerdetailsrecommendations。/media/customerdetailsrecommendations.png)](。/media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>配置操作的 Dynamics 365 可以启用建议 POS
若要设置产品建议，您需要执行以下。

1.  确保选择正确**法人**。
2.  导航**实体商店** **，选择零售**，然后单击"刷新** **。** **使用这将演示数据 (或您的数据) 从您的操作数据库并将其移至实体商店。
3.  选项：若要查看有关交易记录建议的屏幕，请转到**屏幕布局，**选择您的屏幕布局，启动**屏幕布局设计器** ** **，然后可取消**建议控制**从中需要。
4.  **转到零售参数**选择**，机器学习** **，选择是** **下建议** POS 启用"。
5.  查看在 POS 上建议，全局配置运行作业** ** 1110。 若要给反映变化进行 POS 屏幕布局设计器，通道配置运行作业** ** 1070。

## <a name="how-does-it-work"></a>[] () 工作原理？
在您刷新**实体商店**实体时，发生以下操作。

-   认知在服务所需的格式导出数据从工序 365 的 Dynamics 数据库提取实体和发送到商店。
-   作为 ADF 活动的一部分，数据 Azure 的数据中心用于 (ADF) 数据洗涤使用配置单元脚本。 将洗涤的数据在一滴存储中。
-   从一个滴存储数据的 API 认知的培训建议用于服务模型。

在打开**启用"建议**和运行作业配置时，发生以下操作。

-   模型 ID 凭据并从 API 将领取和存储在工序的 Dynamics 365 数据库，在 AOS 的 web.config，然后在"零售服务器。
-   模型 ID 凭据并为有效 CRT，以便以联机方式的呼叫从产品{{请求：for}}云 POS 的建议和端可以承兑。


<a name="see-also"></a>请参阅
--------

[请添加一控件。建议在 POS 设备] (添加建议控制 POS screen.md) 的交易记录页


