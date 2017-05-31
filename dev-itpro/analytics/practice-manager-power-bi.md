---
title: "实践经理 Power BI 内容"
description: "此主题介绍实践经理 Power BI 内容中的内容。 它说明如何访问内容包中包括的报表，并提供有关用于构建内容包的数据模型和实体的信息。"
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>实践经理 Power BI 内容

[!include[banner](../includes/banner.md)]


此主题介绍**实践经理** Microsoft Power BI 内容中的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="overview"></a>概览

**实践经理** Power BI 内容为实践经理和项目经理创建。 它提供与组织正在处理的项目相关的关键指标。 仪表板提供了项目以及相关客户的概览。 报表级筛选器可用于特定法人的报表。 此 Power BI 内容从 Microsoft Dynamics 365 for Operations 的项目核算聚合度量拉取数据。

**实践经理** Power BI 内容包含五个报表页：一个概览页，四个提供项目成本、收入、挣值管理，以及跨各个维度划分和细分的工时指标的详细信息。

内容中的所有金额都以系统币种显示。 您可以在**系统参数**页设置系统币种。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容

Microsoft Dynamics Lifecycle Services (LCS) 中的共享资产库内包含**实践经理** Power BI 内容。 有关如何下载该内容包并将其连接到您的 Dynamics 365 for Operations 数据的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。

若要观看显示如何实现 Power BI 内容的演示，请参阅 [Dynamics Lifecycle Services 中来自 Microsoft 和您的合作伙伴的 Power BI 内容](https://mix.office.com/watch/9puyb1b2xs1w) Office mix。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的报表

下表提供有关在**实践经理** Power BI 内容中的每个报表页找到的度量的详细信息。

| 报表页                                          | 指标               |
|------------------------------------------------------|-----------------------------------------------|
| 仪表板  | 已创建的项目<br>已评估的项目<br>正在进行的项目<br>按阶段划分的项目的数量<br>按城划分的项目的数量<br>按客户显示的实际收入<br>按项目显示的预算毛利<br>挣值管理概览 |
| 成本                                                 | 按月份显示的实际与预算成本<br>按年份显示的实际与预算成本<br>按类别显示的实际与预算成本<br>按交易记录类型显示的实际成本       |
| 收入                                              | 按月份显示的实际收入<br>按邮政编码显示的实际收入<br>按类别显示的实际与预算收入<br>按客户行业显示的实际收入        |
| EVM                                                  | 按项目显示的成本和计划绩效指数                 |
| 工时                                                | 实际收费有偿工时数、实际收费无偿工时数与预算工时<br>按项目划分的实际收费有偿工时数与实际收费无偿工时数<br>按资源划分的实际收费有偿工时数与实际收费无偿工时数<br>按项目划分的实际收费工时比率<br>按资源划分的实际收费工时比率 |

所有这些报表中的图表和磁贴均可以筛选和并固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/)。 您还可以使用“导出基础数据”功能导出在可视化中汇总的基础数据。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体

Dynamics 365 for Operations 数据用于填充**实践经理** Power BI 内容中的报表页面。 这些数据表示为实体商店（这是针对分析进行了优化的 Microsoft SQL 数据库）中暂存的聚合度量。 有关详细信息，请参阅 [Power BI 与实体商店集成概览](power-bi-integration-entity-store.md)。

以下部分说明用于每个实体的聚合度量。

### <a name="entity-projectaccountingcubeactualhourutilization"></a>实体：ProjectAccountingCube_ActualHourUtilization
**数据源**：ProjEmplTrans

| 关键聚合度量                | 字段                                | 说明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | 实际收费有偿工时数总计 |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | 实际负担总计比率             |

### <a name="entity-projectaccountingcubeactuals"></a>实体：ProjectAccountingCube_Actuals
**数据源**：ProjTransPosting

| 关键聚合度量                | 字段                                | 说明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  已过帐的所有交易收入的总计 |   
| ActualCost   |                             Sum(ActualCost)           |    已过帐的所有交易记录类型的成本总计    |

### <a name="entity-projectaccountingcubecustomer"></a>实体：ProjectAccountingCube_Customer
**数据源**：CustTable

| 关键聚合度量                | 字段                                | 说明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    项目数量        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         可用项目计数    |


### <a name="entity-projectaccountingcubeforecasts"></a>实体：ProjectAccountingCube_Forecasts
**数据源**：ProjTransBudget

| 关键聚合度量                | 字段                                | 说明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       预测的所有交易记录类型的成本总计     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    预测应计/开票收入的总计         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |总预测收入总和与总预测成本总和之间的差异。

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>实体：ProjectAccountingCube_ProjectPlanCostsView
**数据源**：项目

| 关键聚合度量                | 字段                                | 说明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | 含计划任务在内估计的所有项目交易记录类型的总成本价 |

### <a name="entity-projectaccountingcubeprojects"></a>实体：ProjectAccountingCube_Projects
**数据源**：项目

| 关键聚合度量                | 字段                                | 说明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   成本绩效指数  |ProjectAccountingCube_Projects[挣值] / ProjectAccountingCube_Projects[已完成任务的总实际成本] |     计算为总挣值除以总实际成本|
|  计划绩效指数 |ProjectAccountingCube_Projects[挣值] / ProjectAccountingCube_Projects[已完成任务的总计划成本]|计算为总挣值除以总计划成本 |
|已完成工作的百分比 |工作完成百分比 = ProjectAccountingCube_Projects[已完成任务的总实际成本] / (ProjectAccountingCube_Projects[已完成任务的总实际成本] + ProjectAccountingCube_Projects[项目的总计划成本] - ProjectAccountingCube_Projects[已完成任务的总计划成本])|已完成工作的总百分比基于已完成任务的总实际成本和项目的计划成本|
|项目实际收费工时比率|ProjectAccountingCube_Projects[项目实际收费有偿工时总数] / (ProjectAccountingCube_Projects[项目实际收费有偿工时总数] + ProjectAccountingCube_Projects[项目实际收费无偿工时总数])|基于有偿 + 无偿的实际收费工时总数|
|挣值|ProjectAccountingCube_Projects[项目的总计划成本] * ProjectAccountingCube_Projects[已完成工作的百分比]|总计划成本乘以已完成工作的百分比。|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>实体：ProjectAccountingCube_TotalEstimatedCosts 
**数据源**：ProjTable

| 关键聚合度量                | 字段                                | 说明                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   含已完成任务在内估计的所有项目交易记录类型的总成本价|

## <a name="additional-resources"></a>其他资源

以下是与实体和构建 Power BI 内容相关的一些有用的链接：

- [数据实体](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [为工作区配置 Power BI 集成](configure-power-bi-integration.md)

