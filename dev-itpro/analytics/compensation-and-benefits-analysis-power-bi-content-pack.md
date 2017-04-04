---
title: "薪酬福利和 Power BI 的内容"
description: "此主题描述工序的 Dynamics 365 和-薪酬福利于 Power BI 的内容。 该说明如何访问在内容包包括的报表，并提供有关用于创建内容包的数据模型和实体的信息。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 557f9218032e2b1160b6ea0631ada951353d2afd
ms.lasthandoff: 03/31/2017


---

# <a name="compensation-and-benefits-power-bi-content"></a>薪酬福利和 Power BI 的内容

此主题描述工序的 Dynamics 365 和-薪酬福利于 Power BI 的内容。 该说明如何访问在内容包包括的报表，并提供有关用于创建内容包的数据模型和实体的信息。

<a name="accessing-the-content-pack"></a>访问内容包
--------------------------

您在 Microsoft Dynamics Lifecycle Services (LCS) 可以查找和薪酬福利内容包在共享资产的库中。 有关如何下载内容包和将它连接的详细信息。您的工序数据的 Microsoft Dynamics 365，请参阅在 [LCS 的 Power BI 的内容是从 Microsoft 和您的合作伙伴] (Microsoft partners.md BI 的内容。)

## <a name="reports-that-are-included-in-the-content-pack"></a>内容包包括报表。
在连接内容包到您的工序数据的 Dynamics 365 后，报表查看组织的数据。 如果您选择"从不使用 Microsoft Power BI "，您可以了解在此{{对：about}}引导了解 Power BI 的 [] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData) 页。 在内容包包括的报表具有包含附加信息的两个图表和表。 下表对报表进行了描述。

| 报告                     | 内容                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| 第效益和分析 | 按公司、平均小时工资、平均包含的员工按付工资、雇用类型和计划登记的每小时工资和包含的员工 |
| 员工福利          | 按所选员工福利的登记                                                                                               |

您可以筛选平铺和图表，这些报表和单边锁定图表和平铺到仪表板。 有关如何筛选和单边锁定的更多信息的详细信息。Power BI，请参阅创建和配置 [] (https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards) 仪表板。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
工序数据的 Dynamics 365:用于填充时，会在薪酬福利压缩和内容的报告。 下表显示实体，内容包基础。

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
| 人才\_PastPositionAssignment | 分配原因、开始日期、结束日期和作业                                                           | 人才\_CalendarOffset 人才\_日期\_人才作业\_人才职位                                                                                                                                                                                                                                                     |
| 人才\_性能            | 等级、该代码的描述和该评级模型                                                                      | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 人才\_职位               | 部门、FTE、职位、职位类型和标题                                                        | 人才\_CurrentPosition 人才\_CurrentWorker                                                                                                                                                                                                                                                                              |
| 人才\_PositionTrend          | 随着时间的推移，职位 FTE 和工作                                                                          | 人才\_CalendarOffset 人才\_日期\_人才作业\_人才职位                                                                                                                                                                                                                                                     |
| 人才\_ReportsToWorkerName    | 名、姓氏全名和                                                                       | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 人才\_技能                  | 技能、技能类型和等级                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| 人才\_TerminatedWorker       | 终止的工人、结束日期、标题、职位和工作                                             | 人才\_公司员工\_薪酬\_人才 GeographicLocation 人才\_性能\_人才 WorkerName 人才\_ReportsToWorkerName 人才\_CalendarOffset 人才\_日期\_人才 WorkerTitle 人才\_人口统计学人才\_雇用员工\_作业\_人才职位\_WorkerBenefit 人才 |
| 人才\_WorkerBenefit          | 生效日期、福利选项、福利计划并且福利类型                                             | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 人才\_WorkerName             | 名、姓氏全名和                                                                       | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 人才\_WorkerTitle            | 页眉和资历日期                                                                                   | 人才\_CurrentWorker 人才\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | 工作人员随着时间的推移，总人数、公司和职位                                                        | 人才\_公司员工\_薪酬\_人才 GeographicLocation 人才\_性能\_人才 WorkerName 人才\_ReportsToWorkerName 人才\_CalendarOffset 人才\_日期\_人才 WorkerTitle 人才\_人口统计学人才\_雇用员工\_作业\_WorkerBenefit 人才                     |

这些实体用于创建在数据模型的计算度量值。 这些计算度量值随后将用于计算在内容包的关键绩效指标 (KPI) 和报表。 如果您需要对您包括的报表和仪表板的其他计算，可以下载并修改了 CompensationandBenefits.pbix LCS 的文件。 此文件是用于创建内容包的默认数据模型。 在您进行了修改后，可以创建包含信息您已添加的有组织内容包和仪表板。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



