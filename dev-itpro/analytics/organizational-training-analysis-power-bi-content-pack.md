---
title: Organizational Training Power BI content
description: "此主题描述操作的节点-组织培训 Power BI 内容 Dynamics 365。 该说明如何访问内容包，并描述用于创建内容包的数据模型和实体。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Organizational Training Power BI content

此主题描述操作的节点-组织培训 Power BI 内容 Dynamics 365。 该说明如何访问内容包，并描述用于创建内容包的数据模型和实体。

<a name="accessing-the-content-pack"></a>访问内容包
--------------------------

您在 Microsoft Dynamics Lifecycle Services (LCS) 可以找到组织培训内容包在共享资产的库中。 有关如何下载内容包和将它连接的详细信息。您的工序数据的 Microsoft Dynamics 365，请参阅在 [LCS 的 Power BI 的内容是从 Microsoft 和您的合作伙伴] (Microsoft partners.md BI 的内容。)

## <a name="reports-that-are-included-in-the-content-pack"></a>内容包包括报表。
在连接内容包到您的工序数据的 Dynamics 365 后，报表查看组织的数据。 如果您选择"从不使用 Microsoft Power BI "，您可以了解在此{{对：about}}引导了解 Power BI 的 [] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData) 页。 在内容包包括的报表具有包含附加信息的两个图表和表。 下表对报表进行了描述。

| 报告          | 内容                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| 课程分析 | 按库位登记，按状态的课程参与者和登记列表 |
| 课程类型    | 课程类型(按技能)                                                       |

您可以筛选平铺和图表，这些报表和单边锁定图表和平铺到仪表板。 有关如何筛选和单边锁定的更多信息的详细信息。Power BI，请参阅创建和配置 [] (https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards) 仪表板。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
工序数据的 Dynamics 365:用于填充时，会在组织培训内容包的报表。 下表显示实体，内容包基础。

| 实体                    | 内容                                                         | 关系具有其他实体                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 培训\_CalendarOffset  | 为希望将切片报表的偏移日历                                | 培训\_培训\_CourseAttendees 的 CourseAgenda                                                                                                                                                   |
| 培训\_公司         | 筛选报表的公司                                    | 培训\_培训\_CourseAttendees 的 CourseAgenda                                                                                                                                                   |
| 培训课程\_          | 课程、描述、教师姓名、地点、教室和省/市/自治区 | 培训\_培训\_CourseAttendees 的 CourseAgenda 培训\_CourseSkill                                                                                                                             |
| 培训\_CourseAgenda    | 课程安排、课程和开始时间和结束时间                          | 培训\_培训 CalendarOffset 的公司\_培训\_培训课程的\_日期                                                                                                                         |
| 培训\_CourseAttendees | 名称、状态、作业和登记日期                         | 培训\_培训 CalendarOffset 的公司\_培训培训\_人口统计学的日期\_培训\_培训课程的\_雇用培训\_培训\_WorkerTitle 的 WorkerName 培训\_工作培训\_职位 |
| 培训\_CourseSkill     | 技能、技能类型和级别                                     | 培训课程\_                                                                                                                                                                                   |
| 培训\_日期            | 天、周、在职个月和年                                   | 培训\_培训\_CourseAttendees 的 CourseAgenda                                                                                                                                                   |
| 培训\_人口统计学    | 出生日期、性别、婚姻状况血统和种族         | 培训\_培训\_CourseAttendees 的 CourseAgenda                                                                                                                                                   |
| 培训\_雇用      | 日期、开始过渡日期和结束日期                        | 培训\_培训\_CourseAttendees 的 CourseAgenda                                                                                                                                                   |
| 培训\_作业             | 功能、类型和标题                                        | 培训\_培训\_CourseAttendees 的 CourseAgenda                                                                                                                                                   |
| 培训\_职位        | 职位、职务和等效的全职 (FTE)                  | 培训\_培训\_CourseAttendees 的 CourseAgenda                                                                                                                                                   |
| 培训\_WorkerName      | 名、姓氏全名和                             | 培训\_CourseAttendees                                                                                                                                                                          |
| 培训\_WorkerTitle     | 页眉和资历日期                                         | 培训\_CourseAttendees                                                                                                                                                                          |

这些实体用于创建在数据模型的计算度量值。 这些计算度量值随后将用于计算在内容包的关键绩效指标 (KPI) 和报表。 如果您需要对您包括的报表和仪表板的其他计算，可以下载并修改了 Training.pbix LCS 的文件。 此文件是用于创建内容包的默认数据模型。 在您进行了修改后，可以创建包含信息您已添加的有组织内容包和仪表板。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



