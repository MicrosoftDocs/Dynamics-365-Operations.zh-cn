---
title: 学习 Power BI 内容
description: 此主题描述学习 Power BI 内容。
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a4ea4606f9987bc08565d43a1f05243acf88883c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553755"
---
# <a name="learning-power-bi-content"></a>学习 Power BI 内容

[!include [banner](../includes/banner.md)]

此主题描述**学习** Microsoft Power BI 内容。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的报表

此**学习** Power BI 内容中包含的报表有图表和表，其中包含更多信息。 下表对报表进行了描述。

| 报告                | 内容 |
|-----------------------|----------|
| 学习概览     | 其他报表的汇总 |
| 课程分析       | 按位置分类的登记、按状态分类的参与者、各公司按类型分类的课程，以及按作业分类的课程参与者 |
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
