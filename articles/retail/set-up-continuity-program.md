---
title: "设置呼叫中心的连续性计划"
description: "本文介绍如何为呼叫中心设置连续性计划。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 00504b62237ac4f121d603d5144ffa4e71956cc3
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-a-continuity-program-for-a-call-center"></a>设置呼叫中心的连续性计划

[!include[banner](includes/banner.md)]


本文介绍如何为呼叫中心设置连续性计划。

在连续性计划中，也被称作重复执行订单计划，客户根据预定义的计划收货常规产品装运。 每个装运可以包含不同的产品，如在每月一书俱乐部或相同产品可以重复发送的情况下。 若要设置连续性计划，必须完成以下任务。

1.  在**呼叫中心参数**页设置连续性参数。
2.  创建指定详细信息的连续性计划，如付款计划、装运的时间和是否提前记帐。 还必须添加连续性计划中所包含的产品列表。 每个产品接收一个从 1 开始的连续分配的事件 ID 编号。 事件 ID 决定产品发送的顺序。
    -   如果客户在每个装运接收不同产品，产品从当前事件开始基于其事件 ID 按连续顺序发送。
    -   如果客户在每个装运接收相同产品，列表仅包含一个有事件 ID 的产品。 且相同事件重复发生。 可以指定每个事件重复的次数。

3.  创建父产品来表示在任务 2 中创建的连续性计划。 如果添加此产品到销售订单，则**连续性**页打开。 然后可以使用此页创建实际的连续性订单。 父产品不指定该客户在每个装运中接收的单独产品。

在您按照上述说明设置了继续订货之后，您可以为客户创建一个连续性订单。 您也需不得不执行以下这些额外的维护任务。

-   **更新当前连续性事件期间** – 设置告知系统当前事件期间是什么的批处理作业。
-   **创建连续性子订单** – 创建父连续性订单的子订单。
-   **处理连续性付款** – 处理与连续性销售订单关联的帐单和通知。
-   **扩展连续性行**（如果要求）– 扩展连续性事件可重复的次数。 重复装运可能超过在呼叫中心参数的**连续性重复阈值**字段中设置的限制。
-   **执行连续性更新**（如果要求）– 同步连续性计划和连续性父销售订单之间的更改。
-   **关闭连续性父行和父订单** – 关闭连续性订单。





