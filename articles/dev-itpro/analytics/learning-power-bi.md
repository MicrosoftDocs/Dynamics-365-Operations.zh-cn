---
title: "学习 Power BI 内容"
description: "此主题描述学习 Power BI 内容。 它说明如何访问报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 895cc28cbbdf4ef33c55bc5732e3433d319dca6d
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="learning-power-bi-content"></a>学习 Power BI 内容

[!include[banner](../includes/banner.md)]

此主题描述**学习** Microsoft Power BI 内容。 它说明如何访问该内容，并描述用于构建该内容的数据模型和实体。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容

如果您使用的是 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月），您可以查找 Microsoft Dynamics Lifecycle Services (LCS) 共享资产库中的**学习** Power BI 内容。 有关如何下载内容并在您的组织中实现的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。 若要观看显示如何实现 Power BI 内容的演示，请参阅 [Dynamics Lifecycle Services 中来自 Microsoft 和您的合作伙伴的 Power BI 内容](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的报表

**学习** Power BI 内容中包含的报表有图表和表，其中包含更多信息。 下表对报表进行了描述。

| 报告                | 内容 |
|-----------------------|----------|
| 学习概览     | 其他报表的汇总 |
| 课程分析       | 按位置分类的登记、按状态分类的参与者、各公司按类型分类的课程，以及按作业分类的课程参与者 |
| 登记分析 | 登记列表 |
| 课程类型          | 课程类型(按技能) |
| 教师分析   | 课程与教师的比率、教师数量、按教师分类的课程、各教师的课程，以及按教师分类的课程安排 |
| 提供的课程       | 课程列表 |
| 课程设计        | 课程安排 |

可以筛选这些报表中的图表和磁贴，并将图表和磁贴固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体

以下数据用于填充**学习** Power BI 内容中的报表。 此表显示内容所基于的实体。

| 实体           | 内容                                                         | 与其他实体之间的关系 |
|------------------|------------------------------------------------------------------|-----------------------------------|
| 日历偏差  | 要切分的日历偏差报表                                | 课程安排、课程参与者 |
| 公司          | 充当报表筛选依据的公司                                   | 课程安排、课程参与者 |
| 课程           | 课程、描述、教师姓名、位置、教室和状态 | 课程安排、课程参与者、课程技能 |
| 课程安排    | 课程安排、课程和开始时间和结束时间                          | 公司、日历偏差、日期、课程 |
| 课程参与者 | 名称、状态、作业和登记日期                         | 公司、日历偏差、日期、课程、人口统计学、雇用、课程、员工姓名、员工职务、作业、职位 |
| 课程技能     | 技能、技能类型和级别                                     | 课程 |
| 日期             | 天数、周数、月数和年数                                   | 课程安排、课程参与者 |
| 人口统计数据     | 生日、性别、种族和婚姻状况         | 课程安排、课程参与者 |
| 雇用       | 开始日期、结束日期和转换日期                        | 课程安排、课程参与者 |
| 作业              | 功能，类型和标题                                        | 课程安排、课程参与者 |
| 位置         | 职位、职务和全职等效 (FTE)                  | 课程安排、课程参与者 |
| 员工姓名    | 名字、姓氏和全名                             | 课程参与者 |
| 员工职务   | 职务和资历日期                                         | 课程参与者 |

这些实体用于在数据模型中创建计算度量值。 然后，这些计算的度量值用于计算在内容中使用的关键绩效指标 (KPI) 和报表。 如果要在报表和仪表板中包含更多计算，可以从 LCS 下载 .pbix 文件并修改。 此文件是用于创建内容的默认数据模型。 修改后，可以创建包含您已添加的信息的组织内容包和仪表板。

