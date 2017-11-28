---
title: "实践经理 Power BI 内容"
description: "此主题介绍实践经理 Power BI 内容中的内容。 它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3462ef1bbde9a98ac6a7bc9a5c54e58ff98559c8
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="practice-manager-power-bi-content"></a>实践经理 Power BI 内容

[!include[banner](../includes/banner.md)]

此主题介绍**实践经理** Microsoft Power BI 内容中的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="overview"></a>概览

**实践经理** Power BI 内容为实践经理和项目经理创建。 它提供与组织正在处理的项目相关的关键指标。 仪表板提供了项目以及相关客户的概览。 报表级筛选器可用于特定法人的报表。 此 Power BI 内容从项目核算聚合度量中提取数据。

**实践经理** Power BI 内容包含五个报表页：一个概览页，四个提供项目成本、收入、挣值管理，以及跨各个维度细分的工时指标的详细信息。

内容中的所有金额都以系统币种显示。 您可以在**系统参数**页设置系统币种。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容
如果您正在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月），则**实践经理** Power BI 内容在**实践管理**工作区显示。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的报表

下表提供有关在**实践经理** Power BI 内容中的每个报表页找到的度量的详细信息。

| 报表页       | 指标 |
|-------------------|---------|
| 项目概览 | <ul><li>已创建的项目</li><li>已评估的项目</li><li>正在进行的项目</li><li>按阶段划分的项目的数量</li><li>按城划分的项目的数量</li><li>按客户显示的实际收入</li><li>按项目显示的预算毛利</li><li>挣值管理概览</li></ul> |
| 成本              | <ul><li>按月份显示的实际与预算成本</li><li>按年份显示的实际与预算成本</li><li>按类别显示的实际与预算成本</li><li>按交易记录类型显示的实际成本</li></ul> |
| 收入           | <ul><li>按月份显示的实际收入</li><li>按邮政编码显示的实际收入</li><li>按类别显示的实际与预算收入</li><li>按客户行业显示的实际收入</li></ul> |
| EVM               | 按项目显示的成本和计划绩效指数 |
| 工时             | <ul><li>实际收费有偿工时数、实际收费无偿工时数与预算工时</li><li>按项目划分的实际收费有偿工时数与实际收费无偿工时数</li><li>按资源划分的实际收费有偿工时数与实际收费无偿工时数</li><li>按项目划分的实际收费工时比率</li><li>按资源划分的实际收费工时比率</li></ul> |

所有这些报表中的图表和磁贴均可以筛选和并固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/)。 您还可以使用“导出基础数据”功能导出在可视化中汇总的基础数据。

## <a name="extending-the-power-bi-content"></a>扩展 Power BI 内容
使用在 Microsoft Dynamics Lifecycle Services (LCS) 中可用的内容包可以对未登录到 Microsoft Dynamics 365 的人员提供出色的分析。 您可以修改这些内容包，使它们包含其他报表或视觉对象，然后将其发布到您的 Power BI.com 租户进行分析。 

可在 LCS 中的共享资产库内找到**实践经理** Power BI 内容。 有关如何下载内容并在您的组织中实现的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。 若要观看显示如何实现 Power BI 内容的演示，请参阅 [Dynamics Lifecycle Services 中来自 Microsoft 和您的合作伙伴的 Power BI 内容](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix。

请确保下载适用于您使用的 Dynamics 365 版本的**实践经理**内容。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体

以下数据用于填充**实践经理** Power BI 内容中的报表页。 此数据表示为实体商店内已分组的聚合度量。 实体商店是针对分析进行优化的 Microsoft SQL Server 数据库。 有关详细信息，请参阅 [Power BI 与实体商店集成概览](power-bi-integration-entity-store.md)。

以下部分说明用于每个实体的聚合度量。

### <a name="entity-projectaccountingcubeactualhourutilization"></a>实体：ProjectAccountingCube_ActualHourUtilization
**数据源：**ProjEmplTrans

| 关键聚合度量      | 字段                              | 说明 | 
|--------------------------------|------------------------------------|-------------|
| 实际收费有偿工时数 | Sum(ActualUtilizationBillableRate) | 实际收费有偿工时数总计。 |
| 实际收费无偿工时数   | Sum(ActualBurdenBillableRate)      | 实际负担总计比率。 |

### <a name="entity-projectaccountingcubeactuals"></a>实体：ProjectAccountingCube_Actuals
**数据源：**ProjTransPosting

| 关键聚合度量 | 字段              | 说明 | 
|---------------------------|--------------------|-------------|
| 实际收入            | Sum(ActualRevenue) | 已过帐的所有交易收入的总计。 |   
| 实际成本               | Sum(ActualCost)    | 已过帐的所有交易记录类型的成本总计。 |

### <a name="entity-projectaccountingcubecustomer"></a>实体：ProjectAccountingCube_Customer
**数据源：**CustTable

| 关键聚合度量 | 字段                                            | 说明 | 
|---------------------------|--------------------------------------------------|-------------|
| 项目数量        | COUNTA(ProjectAccountingCube_Projects[PROJECTS]) | 可用项目计数。 |


### <a name="entity-projectaccountingcubeforecasts"></a>实体：ProjectAccountingCube_Forecasts
**数据源：**ProjTransBudget

| 关键聚合度量 | 字段                  | 说明 | 
|---------------------------|------------------------|-------------|
| 预算成本               | Sum(BudgetCost)        | 预测的所有交易记录类型的成本总计。 |
| 预算收入            | Sum(BudgetRevenue)     | 预测应计/开票收入的总计。  |
| 预算毛利       | Sum(BudgetGrossMargin) | 总预测收入总和与总预测成本总和之间的差异。 |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>实体：ProjectAccountingCube_ProjectPlanCostsView
**数据源：**项目

| 关键聚合度量 | 字段                    | 说明 | 
|---------------------------|--------------------------|-------------|
| 计划成本              | Sum(SumOfTotalCostPrice) | 含计划任务在内估计的所有项目交易记录类型的总成本价。 |

### <a name="entity-projectaccountingcubeprojects"></a>实体：ProjectAccountingCube_Projects
**数据源：**项目

| 关键聚合度量    | 字段 | 说明 | 
|------------------------------|-------|-------------|
| 成本绩效指数       | ProjectAccountingCube_Projects[挣值] / ProjectAccountingCube_Projects[已完成任务的总实际成本] | 计算为总挣值除以总实际成本。 |
| 计划绩效指数   | ProjectAccountingCube_Projects[挣值] / ProjectAccountingCube_Projects[已完成任务的总计划成本] | 计算为总挣值除以总计划成本。 |
| 已完成工作的百分比 | 工作完成百分比 = ProjectAccountingCube_Projects[已完成任务的总实际成本] / (ProjectAccountingCube_Projects[已完成任务的总实际成本] + ProjectAccountingCube_Projects[项目的总计划成本] - ProjectAccountingCube_Projects[已完成任务的总计划成本]) | 已完成工作的总百分比，基于已完成任务的总实际成本和项目的计划成本。 |
| 实际收费工时数比率  | ProjectAccountingCube_Projects[项目实际收费有偿工时总数] / (ProjectAccountingCube_Projects[项目实际收费有偿工时总数] + ProjectAccountingCube_Projects[项目实际收费无偿工时总数]) | 总实际计费工时数，基于有偿工时数和无偿工时数。 |
| 挣值                 | ProjectAccountingCube_Projects[项目的总计划成本] * ProjectAccountingCube_Projects[已完成工作的百分比] | 总计划成本乘以已完成工作的百分比。 |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>实体：ProjectAccountingCube_TotalEstimatedCosts 
**数据源：**ProjTable

| 关键聚合度量       | 字段               | 说明 | 
|---------------------------------|---------------------|-------------|
| 已完成活动的计划成本 | Sum(TotalCostPrice) | 含已完成任务在内估计的所有项目交易记录类型的总成本价。 |

