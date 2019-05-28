---
title: 为销售订单预留相同批次
description: 本文说明如何设置产品以对照单个库存批次预留库存。
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d6089d07b0f8bc1a36703b5b1c2f24af72770d5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568297"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a>为销售订单预留相同批次

[!include [banner](../includes/banner.md)]

本文说明如何设置产品以对照单个库存批次预留库存。

相同批次预留可让您针对一批库存为销售订单行保留库存。 例如，订购墙纸的客户可以请求通过同一批次为整个订单供货，以避免各卷墙纸之间出现不一致的情况。 要将产品设置为使用相同的批次预留，以下设置必须在分配给产品的物料模型组、跟踪维度组和存储维度组中有效：

-   **物料模型组** - 物料模型组必须为库存策略选择**预留**字段组中的**相同批次选择**和**合并要求**字段。
-   **跟踪维度组** - 跟踪维度组必须为批号选择**按维度的覆盖范围计划**字段。
-   **存储维度组** - 存储维度组必须为**站点**和**仓库**选择**按维度的覆盖范围计划**字段。

如果在为相同批次选择设置的销售订单行上的产品预留库存，则 Microsoft Dynamics 365 for Finance and Operations 会尝试预留单个库存批次中订购的数量。 还应考虑任何特定的批属性要求。 如果无法从单个批次中填满数量，则将显示**相同批次预留冲突**页面。 此页面描述了这些问题以及为继续预留而采取的措施。 以下条件可能会阻止预留批次：

-   批处置代码将销售的**阻止预留**标记为**已阻止**。
-   根据到期日期以及任何适用的客户适售期，该批次已经到期。 如果物料的物料模型组受先过期先出 (FEFO) 日期控制并且已选择最佳使用日期作为选择标准，则仍可考虑预留该物料。
-   根据到期日期和最佳使用日期以及任何客户适售期，该批次的保质期剩余天数不足。




