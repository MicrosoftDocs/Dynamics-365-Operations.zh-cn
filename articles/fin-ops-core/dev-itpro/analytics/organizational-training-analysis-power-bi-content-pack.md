---
title: 组织培训 Power BI 内容
description: 本文描述财务和运营 - 组织培训 Power BI 内容。
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.openlocfilehash: 2e80810dbeb536dccf6e13b5fca6a85f4858d8da
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267233"
---
# <a name="organizational-training-power-bi-content"></a>组织培训 Power BI 内容

[!include [banner](../includes/banner.md)]

本文描述财务和运营 - 组织培训 Power BI 内容。

## <a name="reports-that-are-included-in-the-content-pack"></a>此内容包中包含的报表
在连接内容包到您的数据后，报表将显示组织的数据。 如果您之前从未使用 Microsoft Power BI，可以通过 [Power BI 的指导学习页](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData)了解更多相关信息。 此内容包中包含的报表有图表和表，其中包含更多信息。 下表对报表进行了描述。

| 报告          | 内容                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| 课程分析 | 按位置分类的登记、按状态分类的课程参与者和登记列表 |
| 课程类型    | 课程类型(按技能)                                                       |

可以筛选这些报表中的图表和磁贴，并将图表和磁贴固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
应用程序数据用于填充组织培训内容包中的报表。 下表显示充当内容包基础的实体。

| 实体                    | 内容                                                         | 与其他实体之间的关系 |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| 培训\_日历偏差  | 要切分的日历偏差报表                                | 培训\_课程安排, 培训\_课程参与者 |
| 培训\_公司         | 充当报表筛选依据的公司                                   | 培训\_课程安排, 培训\_课程参与者 |
| 培训\_课程          | 课程、描述、教师姓名、位置、教室和状态 | 培训\_课程安排, 培训\_课程参与者, 培训\_课程技能 |
| 培训\_课程安排    | 课程安排、课程和开始时间和结束时间                          | 培训\_公司, 培训\_日历偏差, 培训\_日期, 培训\_课程 |
| 培训\_课程参与者 | 名称、状态、作业和登记日期                         | 培训\_公司, 培训\_日历偏差, 培训\_日期, 培训\_人口统计数据, 培训\_雇用, 培训\_课程, 培训\_工作人员姓名, 培训\_工作人员职务, 培训\_作业, 培训\_职位 |
| 培训\_课程技能     | 技能、技能类型和级别                                     | 培训\_课程 |
| 培训\_日期            | 天数、周数、月数和年数                                   | 培训\_课程安排, 培训\_课程参与者 |
| 培训\_人口统计数据    | 生日、性别、种族和婚姻状况         | 培训\_课程安排, 培训\_课程参与者 |
| 培训\_雇用      | 开始日期、结束日期和转换日期                        | 培训\_课程安排, 培训\_课程参与者 |
| 培训\_作业             | 功能，类型和标题                                        | 培训\_课程安排, 培训\_课程参与者 |
| 培训\_职位        | 职位、职务和全职等效 (FTE)                  | 培训\_课程安排, 培训\_课程参与者 |
| 培训\_工作人员姓名      | 名字、姓氏和全名                             | 培训\_课程参与者 |
| 培训\_工作人员职务     | 职务和资历日期                                         | 培训\_课程参与者 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
