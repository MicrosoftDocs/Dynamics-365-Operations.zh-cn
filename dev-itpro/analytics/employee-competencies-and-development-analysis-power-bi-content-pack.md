---
title: "员工能力与发展 Power BI 内容"
description: "此主题描述 Dynamics 365 for Operations - 员工能力与发展 Power BI 内容。 它说明如何访问内容包中包括的报表，并提供有关用于构建内容包的数据模型和实体的信息。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1fd6f978b6a871f9f7d3d5e91ab3e0aac789ae88
ms.lasthandoff: 03/31/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>员工能力与发展 Power BI 内容

[!include[banner](../includes/banner.md)]


此主题描述 Dynamics 365 for Operations - 员工能力与发展 Power BI 内容。 它说明如何访问内容包中包括的报表，并提供有关用于构建内容包的数据模型和实体的信息。

<a name="accessing-the-content-pack"></a>访问内容包
--------------------------

Microsoft Dynamics Lifecycle Services (LCS) 中的共享资产库内包含员工能力与发展内容包。 有关如何下载该内容包并将其连接到您的 Microsoft Dynamics 365 for Operations 数据的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。

## <a name="reports-that-are-included-in-the-content-pack"></a>此内容包中包含的报表
在连接内容包到您的 Dynamics 365 for Operations 数据后，报表将显示组织的数据。 如果您之前从未使用 Microsoft Power BI，请可以通过 [Power BI 的指导学习页](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)了解更多相关信息。 此内容包中包含的报表有图表和表，其中包含更多信息。 下表对报表进行了描述。

| 报告                            | 内容                                               |
|-----------------------------------|--------------------------------------------------------|
| 能力与发展分析 | 按类型分类的团队成员技能类型和团队成员技能 |
| 技能模板                     | 所选员工的技能模板                |
| 技能分析                    | 按类型和等级分类的技能                              |

可以筛选这些报表中的图表和磁贴，并将图表和磁贴固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
Dynamics 365 for Operations 数据用于填充员工能力与发展内容包中的报表。 下表显示充当内容包基础的实体。

| 实体                            | 内容                                                                                                   | 与其他实体之间的关系                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 劳动力\_日历偏置         | 要切分的日历偏差报表                                                                          |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_公司                | 充当报表筛选依据的公司                                                                             |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_能力           | 一段时间的付薪比率和频率                                                                           |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_能力    | 截至当前日期的付薪比率和频率                                                              | 劳动力\_公司 劳动力\_当前薪酬 劳动力\_人口统计数据 劳动力\_工作 劳动力\_职位                                                                                                                                                                                            |
| 劳动力\_当前职位        | 截至当前日期的职位，全职等效 (FTE)，开放职位，以及待填补的职位 | 劳动力\_工作 劳动力\_职位                                                                                                                                                                                                                                                                      |
| 劳动力\_当前工作人员          | 截至当前日期的工作人员，年龄和人数                                                         | 劳动力\_公司 劳动力\_薪酬 劳动力\_地理位置 劳动力\_绩效 劳动力\_个人技能 劳动力\_工作人员姓名 劳动力\_报告对象工作人员姓名 劳动力\_工作人员职务 劳动力\_人口统计数据 劳动力\_工作 劳动力\_雇用 劳动力\_职位                     |
| 劳动力\_日期                   | 天数、周数、月数和年数                                                                             |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_人口统计数据           | 生日、性别、种族和婚姻状况                                                   |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_雇用             | 开始日期、结束日期和转换日期                                                                  |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_地理位置     | 市，县，邮政编码和省/市/自治区                                                           |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_作业                    | 功能，类型和标题                                                                                  |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_作业首选技能      | 重要性、等级、技能和技能等级                                                                 | 劳动力\_技能 劳动力\_作业                                                                                                                                                                                                                                                                         |
| 劳动力\_通过职位分配 | 分配原因，开始日期，结束日期和作业                                                           | 劳动力\_日历偏差 劳动力\_日期 劳动力\_工作 劳动力\_职位                                                                                                                                                                                                                            |
| 劳动力\_绩效            | 评级，描述和评级模型                                                                      |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_个人技能            | 级别、技能级别和日期                                                                               | 劳动力\_技能                                                                                                                                                                                                                                                                                        |
| 劳动力\_个人技能分析    | 已认证、级别、级别日期和技能                                                                    | 劳动力\_工作人员姓名 劳动力\_技能                                                                                                                                                                                                                                                                  |
| 劳动力\_职位               | 部门，FTE，职位，职位类型和标题                                                        |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_职位趋势          | 一段时间的职位，FTE 和工作                                                                          | 劳动力\_日历偏差 劳动力\_日期 劳动力\_工作 劳动力\_职位                                                                                                                                                                                                                            |
| 劳动力\_报告对象工作人员姓名    | 名字、姓氏和全名                                                                       |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_技能                  | 技能、技能类型和评级                                                                              |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_离休工作人员       | 离休工作人员，离休日期，职务，职位和工作                                             | 劳动力\_公司 劳动力\_薪酬 劳动力\_地理位置 劳动力\_绩效 劳动力\_工作人员姓名 劳动力\_报告对象工作人员姓名 劳动力\_日历偏差 劳动力\_日期 劳动力\_工作人员职务 劳动力\_人口统计数据 劳动力\_雇用 劳动力\_工作 劳动力\_职位 |
| 劳动力\_工作人员姓名             | 名字、姓氏和全名                                                                       |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_工作人员职务            | 职务和资历日期                                                                                   |                                                                                                                                                                                                                                                                                                         |
| 劳动力\_工作人员趋势             | 一段时间的工作人员，人数，公司和职位                                                        | 劳动力\_公司 劳动力\_薪酬 劳动力\_地理位置 劳动力\_绩效 劳动力\_工作人员姓名 劳动力\_报告对象工作人员姓名 劳动力\_日历偏差 劳动力\_日期 劳动力\_工作人员职务 劳动力\_人口统计数据 劳动力\_雇用 劳动力\_作业                     |

这些实体用于在数据模型中创建计算度量值。 然后，这些计算的度量值用于计算在数据模型中使用的关键绩效指标 (KPI) 和报表。 如果要在报表和仪表板中包含更多计算，可以从 LCS 下载 CompetenciesandDevelopment.pbix 文件并修改。 此文件是用于创建内容包的默认数据模型。 修改后，可以创建包含您已添加的信息的组织内容包和仪表板。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





