---
title: "组织培训 Power BI 内容"
description: "此主题描述 Finance and Operations - 组织培训 Power BI 内容。 它说明如何访问该内容包，并描述用于构建该内容包的数据模型和实体。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, UnifiedOperations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 26499bf5423bc3711d110bd7e548eda238162b7a
ms.contentlocale: zh-cn
ms.lasthandoff: 06/13/2017


---

# <a name="organizational-training-power-bi-content"></a>组织培训 Power BI 内容

[!include[banner](../includes/banner.md)]


此主题描述 Finance and Operations - 组织培训 Power BI 内容。 它说明如何访问该内容包，并描述用于构建该内容包的数据模型和实体。

<a name="accessing-the-content-pack"></a>访问内容包
--------------------------

Microsoft Dynamics Lifecycle Services (LCS) 中的共享资产库内包含组织培训内容包。 有关如何下载该内容包并将其连接到您的 Microsoft Dynamics 365 for Finance and Operations 数据的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。

## <a name="reports-that-are-included-in-the-content-pack"></a>此内容包中包含的报表
在连接内容包到您的 Dynamics 365 for Finance and Operations 数据后，报表将显示组织的数据。 如果您之前从未使用 Microsoft Power BI，请可以通过 [Power BI 的指导学习页](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)了解更多相关信息。 此内容包中包含的报表有图表和表，其中包含更多信息。 下表对报表进行了描述。

| 报告          | 内容                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| 课程分析 | 按位置分类的登记、按状态分类的课程参与者和登记列表 |
| 课程类型    | 课程类型(按技能)                                                       |

可以筛选这些报表中的图表和磁贴，并将图表和磁贴固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
Finance and Operations 数据用于填充组织培训内容包中的报表。 下表显示充当内容包基础的实体。

| 实体                    | 内容                                                         | 与其他实体之间的关系                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 培训\_日历偏差  | 要切分的日历偏差报表                                | 培训\_课程安排 培训\_课程参与者                                                                                                                                                   |
| 培训\_公司         | 充当报表筛选依据的公司                                   | 培训\_课程安排 培训\_课程参与者                                                                                                                                                   |
| 培训\_课程          | 课程、描述、教师姓名、位置、教室和状态 | 培训\_课程安排 培训\_课程参与者 培训\_课程技能                                                                                                                             |
| 培训\_课程安排    | 课程安排、课程和开始时间和结束时间                          | 培训\_公司 培训\_日历偏差 培训\_日期 培训\_课程                                                                                                                         |
| 培训\_课程参与者 | 名称、状态、作业和登记日期                         | 培训\_公司 培训\_日历偏差 培训\_日期 培训\_人口统计数据 培训\_雇用 培训\_课程 培训\_工作人员姓名 培训\_工作人员职务 培训\_作业 培训\_职位 |
| 培训\_课程技能     | 技能、技能类型和级别                                     | 培训\_课程                                                                                                                                                                                   |
| 培训\_日期            | 天数、周数、月数和年数                                   | 培训\_课程安排 培训\_课程参与者                                                                                                                                                   |
| 培训\_人口统计数据    | 生日、性别、种族和婚姻状况         | 培训\_课程安排 培训\_课程参与者                                                                                                                                                   |
| 培训\_雇用      | 开始日期、结束日期和转换日期                        | 培训\_课程安排 培训\_课程参与者                                                                                                                                                   |
| 培训\_作业             | 功能，类型和标题                                        | 培训\_课程安排 培训\_课程参与者                                                                                                                                                   |
| 培训\_职位        | 职位、职务和全职等效 (FTE)                  | 培训\_课程安排 培训\_课程参与者                                                                                                                                                   |
| 培训\_工作人员姓名      | 名字、姓氏和全名                             | 培训\_课程参与者                                                                                                                                                                          |
| 培训\_工作人员职务     | 职务和资历日期                                         | 培训\_课程参与者                                                                                                                                                                          |

这些实体用于在数据模型中创建计算度量值。 然后，这些计算的度量值用于计算在数据模型中使用的关键绩效指标 (KPI) 和报表。 如果要在报表和仪表板中包含更多计算，可以从 LCS 下载 Training.pbix 文件并修改。 此文件是用于创建内容包的默认数据模型。 修改后，可以创建包含您已添加的信息的组织内容包和仪表板。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





