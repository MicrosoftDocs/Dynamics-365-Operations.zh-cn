---
title: "人才度量 Power BI 的内容"
description: "此主题描述-工序的人才度量 Power BI 内容 Dynamics 365。 该说明如何访问在内容包包括的报表，并提供有关用于创建内容包的数据模型和实体的信息。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d03692e39c51cc4eb0fe23ba263e52de2bf3c3da
ms.lasthandoff: 03/31/2017


---

# <a name="workforce-metrics-power-bi-content"></a>人才度量 Power BI 的内容

此主题描述-工序的人才度量 Power BI 内容 Dynamics 365。 该说明如何访问在内容包包括的报表，并提供有关用于创建内容包的数据模型和实体的信息。

<a name="accessing-the-content-pack"></a>访问内容包
--------------------------

您在 Microsoft Dynamics Lifecycle Services (LCS) 可以找到人才度量内容包在共享资产的库中。 有关如何下载内容包和将它连接的详细信息。您的工序数据的 Microsoft Dynamics 365，请参阅在 [LCS 的 Power BI 的内容是从 Microsoft 和您的合作伙伴] (Microsoft partners.md BI 的内容。)

## <a name="reports-that-are-included-in-the-content-pack"></a>内容包包括报表。
在连接内容包到您的工序数据的 Dynamics 365 后，报表查看组织的数据。 如果您选择"从不使用 Microsoft Power BI "，您可以了解在此{{对：about}}引导了解 Power BI 的 [] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData) 页。 在内容包包括的报表具有包含附加信息的两个图表和表。 下表对报表进行了描述。

| 报告                                           | 内容                                                                                                                                                                                                            |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Analysis "公司"，headcount 部门，位置 | 按公司的按部门的总人数，按位置的总人数，总人数和总人数                                                                                                                           |
| 总人数分析作业，撰写，经理            | 按作业的按步骤的总人数，根据经理的总人数，总人数和总人数                                                                                                                                      |
| 总人数趋势分析                         | 本年度总人数按与公司和将总人数的之前年度的前 12 个月                                                                                                                        |
| 人才人口统计学                           | 按种族血统的总人数年限、性别和前，按经验丰富的状态的总人数，按婚姻状况的总人数，标准学生总人数，编号，平均、在职时间年限女性平均帐龄和大于等于男性员工 |
| 职位分析                                | 按部门的位置，打开打开对填充的职位、有效状态对非活动按 Department、职位和职位                                                                                                   |
| 损耗分析                               | 损耗与去年损耗，离开的人员、平均在职时间年限，离开的人员离开按原因的本年度平均帐龄和员工                                                                   |
| 人员(按部门)                             | 具有一人员的员工编号按部门、职位和分配开始日期和结束日期                                                                                                                       |
| 资历分析                               | 工作通常的年龄按公司和任职时间的列表                                                                                                                                                              |
| 周年纪念日和工作年限               | 按工作员工周年纪念日年限按交易                                                                                                                                                                    |

您可以筛选平铺和图表，这些报表和单边锁定图表和平铺到仪表板。 有关如何筛选和单边锁定的更多信息的详细信息。Power BI，请参阅创建和配置 [] (https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards) 仪表板。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
工序数据的 Dynamics 365:用于填充时，会在内容包人才量化指标的报表。 下表显示实体，内容包基础。

| 实体                            | 内容                                                                                                   | 关系具有其他实体                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 人才\_CalendarOffset         | 为希望将切片报表的偏移日历                                                                          | 人才\_PastPositionAssignment 人才\_PositionTrend Workorce\_WorkerTrend 人才\_TerminatedWorker                                                                                                                                                                                                                     |
| 人才\_公司                | 筛选报表的公司                                                                              | 人才\_CurrentCompensation 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| 人才\_薪酬           | 付薪比率和频率随着时间的推移                                                                           | 人才\_CurrentCompensation 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| 人才\_CurrentCompensation    | 付薪比率截至当前日期和频率                                                              | 人才\_公司员工薪酬\_人才\_人口统计学人才\_作业\_人才职位                                                                                                                                                                                                                            |
| 人才\_CurrentPosition        | 截至当前日期之前 (FTE)、全职的、未结和位置打开对填充的位置的位置 | 人才\_作业\_人才职位                                                                                                                                                                                                                                                                                               |
| 人才\_CurrentWorker          | 截至当前日期和年限、总人数的工人                                                         | 人才\_公司员工\_薪酬\_人才 GeographicLocation 人才\_性能\_人才 WorkerName 人才\_ReportsToWorkerName 人才\_WorkerTitle 人才\_人口统计学人才\_作业\_人才人才\_职位雇用员工\_WorkerBenefit                                            |
| 人才\_日期                   | 天、周、在职个月和年                                                                             | 人才\_PastPositionAssignment 人才\_PositionTrend 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| 人才\_人口统计学           | 出生日期、性别、婚姻状况血统和种族                                                   | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 人才\_雇用             | 日期、开始过渡日期和结束日期                                                                  | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 人才\_GeographicLocation     | 城市、县、邮政编码和省/市/自治区                                                           | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 人才\_作业                    | 功能、类型和标题                                                                                  | 人才\_CurrentPosition 人才\_CurrentWorker                                                                                                                                                                                                                                                                              |
| 人才\_JobPerferredSkill      |                                                                                                            |                                                                                                                                                                                                                                                                                                                                  |
| 人才\_PastPositionAssignment | 分配原因、开始日期、结束日期和作业                                                           | 人才\_CalendarOffset 人才\_日期\_人才作业\_人才职位                                                                                                                                                                                                                                                     |
| 人才\_性能            | 等级、该代码的描述和该评级模型                                                                      | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 人才\_PersonSkill            | 级别和技能                                                                                            | 人才\_技能                                                                                                                                                                                                                                                                                                                 |
| 人才\_PersonSkillAnalysis    | 确认，和技能级别                                                                                | 人才\_技能\_WorkerName 人才                                                                                                                                                                                                                                                                                           |
| 人才\_职位               | 部门、FTE、职位、职位类型和标题                                                        | 人才\_CurrentPosition 人才\_CurrentWorker                                                                                                                                                                                                                                                                              |
| 人才\_PositionTrend          | 随着时间的推移，职位 FTE 和工作                                                                          | 人才\_CalendarOffset 人才\_日期\_人才作业\_人才职位                                                                                                                                                                                                                                                     |
| 人才\_ReportsToWorkerName    | 名、姓氏全名和                                                                       | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 人才\_技能                  | 技能、技能类型和等级                                                                              | 人才\_PersonSkill 人才\_PersonSkillAnalysis                                                                                                                                                                                                                                                                            |
| 人才\_TerminatedWorker       | 终止的工人、结束日期、标题、职位和工作                                             | 人才\_公司员工\_薪酬\_人才 GeographicLocation 人才\_性能\_人才 WorkerName 人才\_ReportsToWorkerName 人才\_CalendarOffset 人才\_日期\_人才 WorkerTitle 人才\_人口统计学人才\_雇用员工\_作业\_人才职位\_WorkerBenefit 人才 |
| 人才\_WorkerBenefit          | 生效日期、福利选项、福利计划并且福利类型                                             | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 人才\_WorkerName             | 名、姓氏全名和                                                                       | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend 人才\_PersonSkillAnalysis                                                                                                                                                                                                                        |
| 人才\_WorkerTitle            | 页眉和资历日期                                                                                   | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | 工作人员随着时间的推移，总人数、公司和职位                                                        | 人才\_公司员工\_薪酬\_人才 GeographicLocation 人才\_性能\_人才 WorkerName 人才\_ReportsToWorkerName 人才\_CalendarOffset 人才\_日期\_人才 WorkerTitle 人才\_人口统计学人才\_雇用员工\_作业\_WorkerBenefit 人才                     |

这些实体用于创建在数据模型的计算度量值。 这些计算度量值随后将用于计算在内容包的关键绩效指标 (KPI) 和报表。 如果您需要对您包括的报表和仪表板的其他计算，可以下载并修改了 CompensationandBenefits.pbix LCS 的文件。 此文件是用于创建内容包的默认数据模型。 在您进行了修改后，可以创建包含信息您已添加的有组织内容包和仪表板。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



