---
title: "将生产订单报告为已完工入库"
description: "完工入库是生产阶段。 在此阶段，从生产订单报告成品和移动到库存。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 19a777a8e58e3c8b848e878956b457a4a730f6e2
ms.lasthandoff: 03/31/2017


---

# <a name="report-production-orders-as-finished"></a>将生产订单报告为已完工入库

完工入库是生产阶段。 在此阶段，从生产订单报告成品和移动到库存。

在生产订单上将成品数量报告为完工入库时，此数量将在库存中更新为现有量。 原始计划订单数量的部分数量可报告为完工入库。 也可以在将数量报告为完工入库时报告具有关联的错误原因的错误数量。 在生产订单达到“报告为完工入库”阶段时，表示在生产订单上不再报告其他数量。
以下特征也与**“完工入库”**流程关联：
-   可以设置与报告的数量成比例的原材料消耗量和时间（反向刷新）
-   可以为已为仓库流程启用的物料生成存储工作。
-   成品的计划或标准成本价值可设置为报告给会计科目。
-   可基于质量关联的设置为报告的数量创建质检订单。

数量将报告到输出位置。 随后，生成仓库工作以将数量从输出位置移至由存储工作的位置指令定义的最终目标位置。

-   在已设置质量关联的情况下将生成订单报告为完工入库时，可以创建质检订单。

## <a name="set-a-production-order-to-reporting-as-finished"></a>将生产订单设置为完工入库
可以通过标准生产订单更新功能、工艺卡日记帐和作业卡日记帐或日记帐**“完工入库”**，将生产订单设置为**“完工入库”**。 也可以在报告生产订单的上一个作业时，通过作业卡终端页和作业卡设备页将阶段更新为**“完工入库”**。 最后，您可以启用**“完工入库”**选项作为手持式仓库设备解决方案的流程。  


