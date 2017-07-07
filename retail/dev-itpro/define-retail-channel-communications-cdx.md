---
title: "定义零售渠道通信 (Commerce Data Exchange)"
description: "本文提供商业数据交换及其组件的概览。 它说明每个组件在 Microsoft Dynamics 365 for Retail 和零售渠道之间的数据传输中所扮演的角色。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 68252e52da47b89166627edbf2aa530e762354c6
ms.contentlocale: zh-cn
ms.lasthandoff: 06/20/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>定义零售渠道通信 (Commerce Data Exchange)

[!include[banner](../includes/banner.md)]


本文提供商业数据交换及其组件的概览。 它说明每个组件在 Microsoft Dynamics 365 for Retail 和零售渠道之间的数据传输中所扮演的角色。

<a name="overview"></a>概览
--------

Commerce Data Exchange 是一种在 Dynamics 365 for Retail 和零售渠道（例如，在线商店或实体商店）之间传送数据的系统。 用于存储零售渠道数据的数据库不同于 Dynamics 365 for Retail 数据库。 该渠道数据库仅包含零售交易记录所需的数据。 主数据将在 Dynamics 365 for Retail 中配置并分配到渠道。 交易记录数据将在销售点 (POS) 系统或在线商店中创建，然后上载到 Dynamics 365 for Retail。 数据分配是异步的。 换言之，在源处收集和打包数据的流程独立于在目标处接收和应用数据的流程执行。 对于某些方案（例如价格和库存查找），必须实时检索数据。 为了支持这些方案，Commerce Data Exchange 还包含一种服务，该服务可实现 Dynamics 365 for Retail 与渠道之间的实时通信。 

[![updated-retail-graphic](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>同步服务
Microsoft SQL Server 对 Dynamics 365 for Retail 数据库的更改跟踪用于确定必须发送到渠道的数据更改。 Dynamics 365 for Retail 根据配送计划打包数据并将其保存到中央存储（Azure Blob 存储）。 单独的批处理使用 Commerce Data Exchange: Async Client 库将此数据包插入到渠道数据库中。 

[![同步服务](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>零售调度

调度作业是用于将数据分配到位置和从位置分配数据的机制。 作业由子作业组成，指定了包含要分配的数据的表和表字段。 Dynamics 365 for Retail 包含满足大多数组织的复制要求的预定义调度作业和子作业。 创建以下类型的预定义作业：

-   **下载作业** - 下载作业将已更改的数据从 Dynamics 365 for Retail 发送到渠道数据库。 通过 SQL Server 更改跟踪来跟踪对记录进行的修改。
-   **上载作业（P 作业）**- 上载作业将销售交易记录从渠道拉入 Dynamics 365 for Retail 数据库中。 P 作业以递增方式上载数据。 当 P 作业运行时，Async Client 库将检查已从位置接收的记录的复制计数器。 仅在记录的复制计数器大于找到的最大值时上载记录。 P 作业不会更新以前上载的数据。

配送计划用于手动或通过在 Dynamics 365 for Retail 中计划批处理作业来执行数据传输。 一个分配计划可包含一个或多个渠道数据组以及一个或多个调度作业。

## <a name="realtime-service"></a>实时服务
Commerce Data Exchange: Real-time Service 是一项集成服务，该服务在 Dynamics 365 for Retail 和零售渠道之间提供实时通信。 利用 Real-time Service，各个 POS 计算机和在线商店能够从 Dynamics 365 for Retail 实时检索特定数据。 虽然大多数关键操作可在本地渠道数据库中执行，但以下情况需要直接访问存储在 Dynamics 365 for Retail 中的数据：

-   发放和兑换礼品卡。
-   兑换会员积分。
-   签发和兑换贷项通知单。
-   创建和更新客户记录。
-   创新、更新和完成销售订单。
-   接收针对采购订单或转移单的库存。
-   执行库存计数。
-   检索各个商店的销售交易记录并完成退货交易记录。

[![Real-time Service](./media/rts.png)](./media/rts.png) 

创建预定义的 Real-time Service 模板。




