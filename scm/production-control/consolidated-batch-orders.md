---
title: "合并的批次订单"
description: "本文介绍合并的批次订单的概念。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3359f1cd5c3f1ecf25c3f28a366c022826cf895e
ms.lasthandoff: 03/31/2017


---

# <a name="consolidated-batch-orders"></a>合并的批次订单

本文介绍合并的批次订单的概念。

生产的散装物料被视为父物料，而包装的物料被视为子物料。 散装物料和包装物料之间的关系以散装物料转换表示。 此散装物料转换在散装物料本身上定义。  

包装的物料可包装到被视为一个单位的单个大小或多个大小的容器中。 通过合并散装物料的订单，您可以在单个视图中查看所有相关的批次订单，这些订单可帮助您确定任何必须完成的剩余工作。  

合并的批次订单可以包含以下订单的任意组合：

-   单个散装物料订单和多个包装物料订单
-   多个散装物料订单和多个包装物料订单
-   多个散装物料订单和单个包装物料订单
-   仅包装物料订单



