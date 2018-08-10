---
title: "服务级别协议"
description: "在服务级别协议中，客户同意接受基于服务公司记录问题和解决问题的最短响应时间。"
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 63389ed348e9b1bebe00d9aaa9f78b97ac39317b
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="service-level-agreements"></a>服务级别协议        

[!include [banner](../includes/banner.md)]


服务级别协议 (SLA) 是服务公司和服务客户之间的协议。 在 SLA 中，客户同意接受基于服务公司记录问题和解决问题的最短响应时间。

SLA 设置了为客户提供的服务的标准级别，并使服务公司明确何时应完成服务工作。

可以创建任意数目的 SLA 来为服务客户提供不同级别的服务。

## <a name="create-a-service-level-agreement"></a>创建服务级别协议

1.  单击**服务管理** \> **设置** \> **服务协议** \> **服务级别协议**。

2.  在**服务级别协议**字段中，键入服务级别协议的名称。

3.  键入允许附加到服务服务级别协议的服务请求完成时间。 然后，如果您想要基于特定日历的服务级别协议，则选择一个日历。

## <a name="apply-a-service-level-agreement"></a>应用服务级别协议

将 SLA 直接应用到某服务协议。

根据 SLA 来度量您手动创建并附加到具有此 SLA 的某服务协议的服务订单。

您自动创建的服务订单不附加到 SLA。

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>将服务级别协议应用到服务协议

1.  单击**服务管理** \> **常用** \> **服务协议** \> **服务协议**。 选择您要应用 SLA 的服务协议，然后单击**操作窗格**上的**编辑**。

2.  在**服务级别协议**字段中，选择要分配的 SLA。

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>将服务级别协议应用到服务协议组

1.  单击**服务管理** \> **设置** \> **服务协议** \> **服务协议组**。

2.  在**服务级别协议**字段中，选择要分配的 SLA。

## <a name="track-time-on-a-service-order-against-an-sla"></a>根据 SLA 跟踪服务订单的时间

在您为 SLA 分配到的服务协议创建新的服务订单时，启动服务的交货时间间隔，且系统开始跟踪交货时间。 此外，可以设置以下选项：

  - 可以开始和停止有关服务订单的时间记录，以登记服务订单所花费的总时间。

  - 可以监控是否遵循在服务级别协议中设置的时间间隔。

  - 可以定义超过服务级别协议的时间间隔时必须设置的原因代码。

## <a name="see-also"></a>请参阅

[查看对服务级别协议的遵从性](view-compliance-with-service-level-agreements.md)

  



