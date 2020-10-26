---
title: 为服务订单创建物料需求
description: 如果您需要对服务订单预留特定物料，可以创建它的库存物料需求。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18484b637723cef43cad288c08ddfe53cddf9e03
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978475"
---
# <a name="create-item-requirements-for-service-orders"></a>为服务订单创建物料需求 

[!include [banner](../includes/banner.md)]


您可以创建服务订单跟踪和管理为您的客户提供的服务。 如果您需要对服务订单预留特定物料，可以创建它的库存物料需求。 物料需求可以从库存立即消耗，或可以启动生产订单的物料。

通过使用物料需求来代替物料交易记录，您可以计划刚好在实际使用物料之前交货，创建采购订单，在贸易协议框架中包括物料，以及在生产计划中包括物料需求。

服务订单创建物料需求通过项目进行处理。 若要创建服务单物料需求，必须将服务订单附加到项目中去。 您为服务订单创建物料需求后，可以在**项目**窗体中查看所选项目的物料需求。

## <a name="create-an-item-requirement-for-a-service-order"></a>为服务订单创建物料需求

1.  单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。

2.  选择需要创建物料需求的服务订单。

3.  在**操作窗格**中的**发货**选项卡上单击**物料需求**。

4.  在**物料需求**窗体中输入所需物料的信息。 有关特定字段的更多信息，请参阅[物料需求（窗体）](https://technet.microsoft.com/library/aa552021\(v=ax.60\))。

## <a name="create-an-item-requirement-for-a-service-agreement"></a>为服务协议创建物料需求

1.  单击**服务管理** \> **常用** \> **服务协议** \> **服务协议**。

2.  打开需要创建物料需求的服务协议。

3.  在**行**快速选项卡上，单击**添加**创建新行。

4.  在**交易记录类型**字段中选择**物料**。

5.  在**物料设置**字段中，选择**物料需求**。

6.  在**物料编号**字段中，选择该服务协议所需的物料。

7.  在**行明细**快速选项卡上**产品维度**选项卡中的**站点**字段内，为物料选择库存站点。

8.  若要从协议行中创建服务订单，请在**行**快速选项卡中单击**创建服务订单**，然后将相关信息输入到**创建服务订单**窗体中。 


## <a name="see-also"></a>请参阅

[自动创建服务订单](create-service-orders-automatically.md)。

  


