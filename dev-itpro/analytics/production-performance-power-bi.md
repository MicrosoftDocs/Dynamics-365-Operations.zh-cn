---
title: "生产性能 Power BI 内容"
description: "此主题介绍生产性能 Power BI 内容中包含的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1945d137b337508a1850e3e679a60487aecb6b84
ms.openlocfilehash: fa93249d2dba0e6f72d394daa6a125f29a062594
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---

# <a name="production-performance-power-bi-content"></a>生产性能 Power BI 内容

[!include[banner](../includes/banner.md)]

此主题介绍**生产性能** Microsoft Power BI 内容中包含的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="overview"></a>概览

**生产性能** Power BI 内容针对的是组织中负责生产控制的生产经理或个人。

其中包括的报表让您可以使用 Power BI 监控制造工序在及时执行、质量和成本方面的性能。 报表使用来自生产订单和批次订单的交易记录数据，并提供全公司生产指标的聚合视图和按产品和资源分类的指标明细。

Power BI 内容突出显示组织按时完成全部生产的能力。 基于生产计划预测未来绩效。 综合报表提供对因生产导致的产品缺陷以及资源和工序缺陷率的详细洞察。

此 Power BI 内容也可以让您分析生产差异。 生产差异计算为估计成本与实际成本之差。 当生产订单或批次订单达到**已结束**状态时计算生产差异。

**生产性能** Power BI 内容包括源自生产订单和批次订单的数据。 报表不包括与看板生产有关的数据。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容
如果您使用的是 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本2017 年 7 月更新，则**生产性能** Power BI 内容显示在**生产性能**页（**生产控制** > **查询和报表** > **生产性能分析** > **生产性能**）上。 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的指标

**生产性能** Power BI 内容包含一组报表页面。 每个页面中包含一组可视化为图表、磁贴和表的指标。

下表提供其中包括的可视化项的概览。

| 报表页                                | 图表                                               | 磁贴 |
|--------------------------------------------|------------------------------------------------------|-------|
| 生产性能                     | <ul><li>按日期分类的生产数</li><li>按产品和物料组分类的生产数</li><li>按日期分类的已计划生产数</li><li>按准时性和完全性分类的最后 10 个产品</li></ul> | <ul><li>订单总计</li><li>按时且完全 %</li><li>未完成 %</li><li>提前 %</li><li>延期 %</li></ul> |
| 按产品分类的缺陷                         | <ul><li>按日期分类的缺陷率 (ppm)</li><li>按产品和物料组分类的缺陷率 (ppm)</li><li>按日期分类的生产数量</li><li>按有效率排序的前 10 个产品</li></ul> | <ul><li>缺陷率 (ppm)</li><li>有缺陷的数量</li><li>总数量</li></ul> |
| 按产品分类的缺陷趋势                   | 按生产数量分类的缺陷率 (ppm) | 缺陷率 (ppm) |
| 按资源分类的缺陷                        | <ul><li>按日期分类的缺陷率 (ppm)</li><li>按资源和站点分类的缺陷率 (ppm)</li><li>按工序分类的缺陷率 (ppm)</li><li>按缺陷率排序的前 10 个资源</li></ul> | 有缺陷的数量 |
| 按资源分类的缺陷趋势                  | 按加工数量分类的缺陷率 (ppm) | |
| 用于作业单成本计算的生产差异 | <ul><li>按日期和成本组类型分类的生产差异</li><li>按站点和成本组类型分类的生产差异</li><li>具有不利生产差异的前 10 个产品</li><li>按资源分类的前 10 个不利生产差异</li></ul> | <ul><li>实际成本</li><li>生产差异</li><li>生产差异 %</li></ul> |

## <a name="extending-the-power-bi-content"></a>扩展 Power BI 内容
使用在 Microsoft Dynamics Lifecycle Services (LCS) 中可用的内容包可以对未登录到 Microsoft Dynamics 365 的人员提供出色的分析。 您可以修改这些内容包，使它们包含其他报表或视觉对象，然后将内容包发布到您的 Power BI.com 租户进行分析。

可在 LCS 中的共享资产库内找到**生产性能** Power BI 内容。 有关如何下载内容并在您的组织中实现的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。 若要观看显示如何实现 Power BI 内容的演示，请参阅 [Dynamics Lifecycle Services 中来自 Microsoft 和您的合作伙伴的 Power BI 内容](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix。

请确保下载适用于您使用的 Dynamics 365 版本的**生产性能**内容。

> [!NOTE]
> 如果您使用的是 Microsoft Dynamics 365 for Operations 版本 1611，则 KB 4011327 是此 Power BI 内容的先决条件。 登录 LCS 之后，可以在以下位置访问该 KB：https://fix.lcs.dynamics.com/issue/results/?q=kb4011327。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体

以下数据用于**生产性能** Power BI 内容中的报表页。 此数据表示为实体商店内已分组的聚合度量。 实体商店是针对分析进行优化的 Microsoft SQL Server 数据库。 若要了解有关实体商店的详细信息，请参阅 [Power BI 与实体商店的集成](power-bi-integration-entity-store.md)。

下表显示作为 Power BI 内容基础使用的关键聚合度量。

| 实体                   | 关键聚合度量  | Finance and Operations 的数据源 | 字段              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

下表显示如何使用关键聚合度量在该内容的数据集中创建若干计算度量。

| 度量                  | 该度量的计算方法 |
|--------------------------|-------------------------------|
| 生产差异，%   | 总和（‘生产差异’[生产差异]）/ 总和（‘生产差异’[估计成本]） |
| 所有计划订单       | COUNTROWS（‘计划生产订单’） |
| 提前                    | COUNTROWS（筛选器（‘计划生产订单’、‘计划生产订单’[计划的结束日期]\<‘计划生产订单’[要求日期]）） |
| 延迟                     | COUNTROWS（筛选器（‘计划生产订单’，‘计划生产订单’[计划的结束日期]\>‘计划生产订单’[要求日期]）） |
| 按时                  | COUNTROWS（筛选器（‘计划生产订单’，‘计划生产订单’[计划的结束日期] =‘计划生产订单’[要求日期]）） |
| 按时 %                | IF（‘计划生产订单’[按时] \<\> 0，‘计划生产订单’[按时]，IF（‘计划生产订单’[所有计划订单] \<\> 0，0，空白()））/‘计划生产订单’[所有计划订单] |
| 完成                | COUNTROWS（筛选器（‘生产订单’，‘生产订单’[已 RAF] = TRUE）） |
| 缺陷率 (ppm)     | IF（‘生产订单’[总数量] = 0，空白()，（总和（‘生产订单’[有缺陷的数量]）/‘生产订单’[总数量]）\* 1000000） |
| 延期生产率  | ‘生产订单’[延期 \#] /‘生产订单’[已完成] |
| 提前且完全          | COUNTROWS（筛选器（‘生产订单’，‘生产订单’[完全] = TRUE &&‘生产订单’[提前] = TRUE）） |
| 提前 \#                 | COUNTROWS（筛选器（‘生产订单’，‘生产订单’[提前] = TRUE）） |
| 提前 %                  | IFERROR（IF（‘生产订单’[提前 \#] \<\> 0，‘生产订单’[提前 \#]，IF（‘生产订单’[订单总计] = 0，空白()，0））/‘生产订单’[订单总计]，空白()） |
| 未完成               | COUNTROWS（筛选器（‘生产订单’，‘生产订单’[完全] = FALSE &&‘生产订单’[已 RAF] = TRUE）） |
| 未完成 %             | IFERROR（IF（‘生产订单’[未完成] \<\> 0，‘生产订单’[未完成]，IF（‘生产订单’[订单总计] = 0，空白()，0））/‘生产订单’[订单总计]，空白()） |
| 已延迟               | ‘生产订单’[已 RAF] = TRUE &&‘生产订单’[延迟值] = 1 |
| 提前                 | ‘生产订单’[已 RAF] = TRUE &&‘生产订单’[延迟的天数] \< 0 |
| 完全               | ‘生产订单’[完好数量] \>=‘生产订单’[计划的数量] |
| 已 RAF                | ‘生产订单’[生产状态值] = 5 \|\| ‘生产订单’[生产状态值] = 7 |
| 延期和完全           | COUNTROWS（筛选器（‘生产订单’，‘生产订单’[完全] = TRUE &&‘生产订单’[已延迟] = TRUE）） |
| 延期 \#                  | COUNTROWS（筛选器（‘生产订单’，‘生产订单’[已延迟] = TRUE）） |
| 延期 %                   | IFERROR（IF（‘生产订单’[延期 \#] \<\> 0，‘生产订单’[延期 \#]，IF（‘生产订单’[订单总计] = 0，空白()，0））/‘生产订单’[订单总计]，空白()） |
| 按时且完全        | COUNTROWS（筛选器（‘生产订单’，‘生产订单’[完全] = TRUE &&‘生产订单’[已延迟] = FALSE &&‘生产订单’[提前] = FALSE）） |
| 按时且完全 %      | IFERROR（IF（‘生产订单’[按时且完全] \<\> 0，‘生产订单’[按时且完全]，IF（‘生产订单’[已完成] = 0，空白()，0））/‘生产订单’[已完成]，空白()） |
| 订单总计             | COUNTROWS（‘生产订单’） |
| 总数量           | 总和（‘生产订单’[完好数量]）+ 总和（‘生产订单’[有缺陷的数量]） |
| 缺陷率 (ppm)        | IF（‘工艺路线交易记录’[已处理的数量] = 0，空白()，（总和（‘工艺路线交易记录’[有缺陷的数量]）/‘工艺路线交易记录’[已处理的数量]）\* 1000000） |
| 混合缺陷率 (ppm) | IF（‘工艺路线交易记录’[混合数量总计] = 0，空白()，（总和（‘工艺路线交易记录’[有缺陷的数量]）/‘工艺路线交易记录’[混合数量总计]）\* 1000000） |
| 已处理的数量       | 总和（‘工艺路线交易记录’[完好数量]）+ 总和（‘工艺路线交易记录 [有缺陷的数量]） |
| 混合数量总计     | 总和（‘生产订单’[完好数量]）+ 总和（‘工艺路线交易记录 [有缺陷的数量]） |

下表显示用作筛选器以切分聚合度量的关键维度，以便获得粒度更细微，更深入的分析洞察。

| 实体                    | 属性示例                                        |
|---------------------------|---------------------------------------------------------------|
| 完工入库日期 | 完工 (RAF) 日期、月份和年份偏移                 |
| 结束日期                | 已结束月份的偏移和月份                                  |
| 需求日期          | 需求日期月份偏移和需求日期            |
| 工艺路线交易记录日期    | 工艺路线交易记录月份的偏移和日期                       |
| 站点                     | 站点 ID、站点名称、省/市/自治区和城市                          |
| 实体                  | ID 和名称                                                   |
| 资源                 | 资源 ID、资源名称、资源类型和资源组 |
| 产品                  | 产品编号、产品名称、物料 ID 和物料组         |

## <a name="additional-resources"></a>其他资源

以下是与实体和构建 Power BI 内容相关的一些有用的链接：

- [数据实体](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities)
- [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [将 Power BI 磁贴添加到工作区](/dynamics365/unified-operations/dev-itpro/analytics/configure-power-bi-integration)

