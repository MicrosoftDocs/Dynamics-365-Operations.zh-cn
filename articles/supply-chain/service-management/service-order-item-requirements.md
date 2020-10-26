---
title: 服务订单物料需求
description: 如果您需要对服务订单预留特定物料，可以创建它的库存物料需求。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8866d8a4d6ad879f2c43b470af98457cb7c75721
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985732"
---
# <a name="service-order-item-requirements"></a>服务订单物料需求   

[!include [banner](../includes/banner.md)]


您可以创建服务订单跟踪和管理为您的客户提供的服务。 如果您需要对服务订单预留特定物料，可以创建它的库存物料需求。 物料需求可以从库存立即消耗，或可以启动生产订单的物料。

通过使用物料需求来代替物料交易记录，您可以计划刚好在实际使用物料之前交货，创建采购订单，在贸易协议框架中包括物料，以及在生产计划中包括物料需求。

服务订单创建物料需求通过项目进行处理。 若要在服务订单创建物料需求，必须将服务订单附加到项目。

在为服务订单创建某一物料需求后，就可以从单独服务订单中的**项目**或通过**销售订单**窗体查看该物料需求。

## <a name="view-an-item-requirement-from-a-service-order"></a>从服务订单查看物料需求

1.  单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。

2.  单击**发货**，然后单击**物料需求**打开**物料需求**窗体。

3.  单击**项目**选项卡，然后检查**服务订单**字段以查看物料需求的服务订单。

## <a name="delete-service-orders-with-item-requirements"></a>删除具有物料需求的服务订单

如果针对某一服务订单创建物料需求，则不能删除该服务订单。 您必须首先删除物料需求，然后才能删除该服务订单。

1.  单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。

2.  单击**发货**，然后单击**物料需求**打开**物料需求**窗体。 此窗体将列出在该服务订单上创建的物料需求。

3.  选择适当的物料需求行来删除，然后单击**删除**。

–或–

1.  单击**项目管理与核算** \> **通用** \> **项目** \> **所有项目**。

2.  打开具有创建了物料需求的服务订单的项目。

3.  在**项目**窗体中，在右边的窗格，单击**物料需求** 。 **物料需求**窗体将打开，窗体中将列出与所选项目相关联的物料需求。

4.  选择适当的物料需求行来删除，然后单击**删除**。

## <a name="see-also"></a>请参阅

[物料需求（窗体）](https://technet.microsoft.com/library/aa552021\(v=ax.60\))

