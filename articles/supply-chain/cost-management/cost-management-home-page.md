---
title: "成本管理主页"
description: "可通过成本管理处理原材料、半成品、成品和在制品资产的计价和核算。"
author: AndersGirke
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cab2f165a70e5ce8f09f0391282e055e51afb225
ms.openlocfilehash: b1513e5a7cb3a19fd3743a5aac8efd211aa02ce8
ms.contentlocale: zh-cn
ms.lasthandoff: 02/21/2018

---

# <a name="cost-management-home-page"></a>成本管理主页

[!include [banner](../includes/banner.md)]

可通过[成本管理（视频）](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be)处理原材料、半成品、成品和在制品资产的计价和核算。 这是定义、管理和报告[库存会计](cost-object.md)和[制造会计](bom-calculations.md)的过程。

可以在以下区域中定义成本策略： 
-  [预先确定的成本](costing-versions.md)
-  [库存会计](cost-object.md)
-  [制造会计](bom-calculations.md)
-  [间接成本核算](costing-sheets.md)
-  [分类帐集成](production-order-cost-analysis.md)

例如，可定义要在库存核算中应用于[物料类型组](../inventory/reserve-inventory-quantities.md)中的产品的库存计价方法，如[先进先出](fifo-physical-value-marking.md)、[加权平均](weighted-average-physical-value-marking.md)、[标准成本](prerequisites-standard-costs.md)或[移动平均](moving-average.md)。

可从**成本管理**和**成本分析**工作区访问库存核算和制造核算。 这些工作区提供丰富的当前状态、关键绩效指标 (KPI) 和偏差检测的概览。 

可通过制造核算处理生产订单和批次订单中的[作业单成本计算](production-order-cost-analysis.md)，以及 Lean manufacturing 中的[倒冲成本计算法](backflush-costing.md)。

[成本管理 Power BI 内容](../../dev-itpro/analytics/cost-management-content-pack.md)提供对库存和在制品 (WIP) 库存的管理洞察，并按类别介绍一段时间内成本在这些库存中的流向。 也可以将此信息用作财务报表的详细补充。

### <a name="additional-resources"></a>其他资源

#### <a name="whats-new-and-in-development"></a>新增功能和开发中的功能

转到 [Microsoft Dynamics 365 路线图](https://roadmap.dynamics.com/)以了解已发布和正在开发的新功能。 

#### <a name="white-paper"></a>白皮书
[使用成本计算单计算物料清单](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/white-papers/365operationsbomcalsheet)介绍了如何设置包含物料和制造的成本计算单，以及该设置对物料清单计算结果的影响。 为了加强这些主题的说明效果，提供了具体方案和数据，用于演示各种设置和配置的效果。 我们不期望您执行所有这些方案，因为本文提供的详细信息不足，无法配置这些方案。 不过，如果您具备基础知识，则可尝试按照显示顺序播放下面列出的任务指南。 使用阅读本文获得的知识执行物料清单计算分析。 

-  [创建成品](tasks/create-finished-product-2016-02.md)
-  [创建半成品](tasks/create-semi-finished-product-2016-02.md)
-  [创建原材料](tasks/create-raw-materials-2016-02.md)
-  [创建 BOM](tasks/create-boms-2016-02.md)
-  [创建路线](tasks/create-routes-2016-02.md)
-  [通过使用单级结构计算 BOM](tasks/calculate-bom-single-level-structure-2016-02.md)
-  [通过使用多级结构计算 BOM](tasks/calculate-bom-multilevel-structure-2016-02.md)


#### <a name="blogs"></a>博客
您可以在 [Dynamics AX 制造研发团队博客](https://blogs.msdn.microsoft.com/axmfg)和 [Dynamics AX 研发团队中的供应链管理博客](https://blogs.msdn.microsoft.com/dynamicsaxscm)中找到有关成本管理的建议、新闻和其他信息。 尽管一些文章是针对成本管理的旧版本编写的，但相同的概念仍适用，并且过程在当前版本中也是相似的。

#### <a name="task-guides"></a>任务指南
其他帮助在 Finance and Operations 中作为任务指南提供。 若要访问任务指南，请单击任何页面上的“帮助”按钮。


