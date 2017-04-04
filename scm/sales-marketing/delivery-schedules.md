---
title: "交货计划"
description: "当您为单个销售订单、销售报价单或采购订单使用多个交货时，可利用交货计划跟踪订单行数量。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: fbada697060c823b0afdb72d1c0cfd8703f4d527
ms.lasthandoff: 03/31/2017


---

# <a name="delivery-schedules"></a>交货计划

当您为单个销售订单、销售报价单或采购订单使用多个交货时，可利用交货计划跟踪订单行数量。

在多个装运时，必须交付在订单或报价单行的总数量需要使用交货计划。 单独的装运上只按交货行表示。 两个或多个交货行构成了一个交货计划。 交货行可以有不同的交货日期、数量、交货方式以及站点和仓库等存储维度。  

**交货计划示例**

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| 总订单（原始订单行） | 600 把椅子                               |
| 请求的交货计划       | 每月 100 把椅子                     |
| 请求的交货时间范围 | 6 个月，在每个月的第一天 |

在这种情况下，该客户请求跨六个月的期间按批处理 100 把椅子的方式完成 600 把椅子的发货。 若要记录交货要求，您可创建一个交货计划。 在交货计划页上，创建六个单独的交货行。 每个交货行包含 100 把椅子，并指示这 100 把椅子的交货日期。 在这种情况下，在连续六个月的每月第一天抵消每一行。  

在您创建一个交货计划时，原始订单行的类型将自动更改为**“包含多个交货的订单行”**。 此类型的行称作业务行，并用图标标记。 交货行由不同图标标记。 如果您在更改交货行的数量，专线更新商业计划对交货的总数量。 如果贸易协议定义订单的总折扣，则交货规划可以确保您的订单有资格享受折扣，总订单，即使订单拆分到单独的交货。  

具有交货的计划订单是比对交货行处理的。 处理包括过帐装箱单、产品收据和开票。  

具有交货计划的订单和报价单的单据打印输出只显示交货行。 它们不显示原始行（业务行）。 **注意：**此外，当您执行这些操作时，只显示交货行：

-   发布
-   复制页
-   浏览列表页和报表

当您确认销售报价单时，生成的销售订单显示整个交货计划，甚至是具有多个交货的订单行。 此外，整个交货计划都显示在所有主要页面上，如销售订单、销售报价单和采购订单。


