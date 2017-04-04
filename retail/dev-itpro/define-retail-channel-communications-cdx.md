---
title: "定义零售渠道通信 (Commerce Data Exchange)"
description: "本文提供商业数据交换及其组件的概览。 该说明每个组件。数据转移。Microsoft Dynamics 365 之间的扮演工序和零售渠道的角色。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>定义零售渠道通信 (Commerce Data Exchange)

本文提供商业数据交换及其组件的概览。 该说明每个组件。数据转移。Microsoft Dynamics 365 之间的扮演工序和零售渠道的角色。

<a name="overview"></a>概览
--------

Commerce Data Exchange 仍为转移数据。工序和零售渠道的 Dynamics 365 之间，例如商店或砖网络和泥商店的系统。 数据存储为零售渠道数据库的工序不同于数据库的 Dynamics 365。 该渠道数据库仅包含零售交易记录所需的数据。 主数据工序中 Dynamics 365 配置和配送给通道。 交易记录数据。销售点 (POS) 系统或网络，然后创建商店上载到工序的 Dynamics (POS)。 数据分配是异步的。 换言之，在源处收集和打包数据的流程独立于在目标处接收和应用数据的流程执行。 对于某些方案（例如价格和库存查找），必须实时检索数据。 为了支持这些方案，Commerce Data Exchange 还包括启用 Dynamics 365 之间的通信实时操作和通道的服务。 

[] (更新![零售图形。/media/updated 零售 Graphic.png)](。/media/updated 零售 graphic.png)  

## <a name="async-service"></a>同步服务
Microsoft Dynamics 在 SQL Server 跟踪工序 365 的更改的数据库用于确定必须发送到通道的数据更改。 基于分配一计划，但 Dynamics 365 工序包装的数据并将其保存到中央存储期限 (Azure 的一滴存储)。 单独的批处理使用 Commerce Data Exchange: Async Client 库将此数据包插入到渠道数据库中。 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>零售调度

调度作业是用于将数据分配到位置和从位置分配数据的机制。 作业由子作业组成，指定了包含要分配的数据的表和表字段。 工序的 Dynamics 365 包含与公司组织的副本要求的预定义的计划作业和子作业。 创建以下类型的预定义作业：

-   **下载**下载作业发送作业–来自运营的 Dynamics 365 更改可以指导数据库中的数据。 通过 SQL Server 更改跟踪来跟踪对记录进行的修改。
-   **上载作业 (作业) **上载– P 作业以便在通道的销售交易记录分为工序数据库的 Dynamics 365。 P 作业以递增方式上载数据。 当 P 作业运行时，Async Client 库将检查已从位置接收的记录的复制计数器。 仅在记录的复制计数器大于找到的最大值时上载记录。 P 作业不会更新以前上载的数据。

分配计划用于数据传输，手动或由排定在 Dynamics 365 的批处理作业来操作。 一个分配计划可包含一个或多个渠道数据组以及一个或多个调度作业。

## <a name="realtime-service"></a>实时服务
Commerce Data Exchange:实时服务即可用于工序和零售渠道提供 Dynamics 365 之间的通信的一项实时集成的服务。 实时服务即可使各个 POS 网络计算机和商店从工序 365 的 Dynamics 检索特定数据。实时。 尽管大多数主要工序在本地信通数据库中，执行以下方案工序中要求对 Dynamics 365 的直接访问存储在中的数据：

-   发放和兑换礼品卡。
-   兑换会员积分。
-   签发和兑换贷项通知单。
-   创建和更新客户记录。
-   创新、更新和完成销售订单。
-   接收针对采购订单或转移单的库存。
-   执行库存计数。
-   检索各个商店的销售交易记录并完成退货交易记录。

[![Real-time Service](./media/rts.png)](./media/rts.png) 

实时服务预定义的模板创建。


