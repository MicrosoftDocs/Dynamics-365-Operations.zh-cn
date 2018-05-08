---
title: "将生产订单报告为已完工入库"
description: "完工入库是生产阶段。 在此阶段，将报告成品并将其从生产订单移到库存。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 80a882e51332d87835bdfb41a1bb1fcda2471f02
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="report-production-orders-as-finished"></a>将生产订单报告为已完工入库

[!include [banner](../includes/banner.md)]

完工入库是生产阶段。 在此阶段，将报告成品并将其从生产订单移到库存。

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




