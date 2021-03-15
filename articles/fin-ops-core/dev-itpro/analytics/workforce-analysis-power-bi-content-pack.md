---
title: 劳动力指标 Power BI 内容
description: 此主题描述劳动力指标 Power BI 内容。
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorkforceWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d0622cebcfca15acf50cf62e8a77af360d4f1bda
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092783"
---
# <a name="workforce-metrics-power-bi-content"></a>劳动力指标 Power BI 内容

[!include [banner](../includes/banner.md)]

此主题描述 **劳动力指标** Microsoft Power BI 内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容
如果您使用以下其中一种产品，则 **劳动力指标** Power BI 内容显示在 **人事管理** 工作区中：

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的度量
下表显示在每个报表上显示的指标。

| 报告                                           | 指标 |
|--------------------------------------------------|---------|
| 人员指标                                   | 其他报表的汇总 |
| 人数分析公司，部门，位置 | 按公司分类的人数，按部门分类的人数，按位置分类的人数，以及总人数 |
| 人数分析工作，步骤，经理            | 按工作分类的人数，按步骤分类的人数，按经理分类的人数，以及总人数 |
| 人数趋势分析                         | 按公司分类的今年与去年人数，以及过去 12 个月的波动人数 |
| FTE 分析                                     | 全职等效 (FTE) 总计，分配的 FTE 总计，按部门分类的 FTE，过去 12 个月的 FTE，按作业分类的 FTE |
| 劳动力人口统计数据                           | 按年龄和性别分类的人数，按种族分类的人数，按退伍军人状态分类的人数，按婚姻状况分类的人数，全职学生人数，平均在职时间，平均年龄，男女员工的比例，以及员工使用的语言 |
| 职位分析                                | 按部门分类的开放职位，开放待填补的职位，有效到无效的职位，以及按部门分类的职位 |
| 流失分析                               | 今年与去年的流失，流失，按年龄和性别分类的现有员工，离职人员的平均在职时间，本月离职员工以及按原因分类的离职员工 |
| 人员(按部门)                             | 按部门、职位、分配开始和结束日期分类且带人员编号的员工 |
| 资历分析                               | 平均在职时间，在公司的平均工作年限，以及资历表 |
| 员工周年纪念日                           | 本月周年纪念日，下个月周年纪念日，按工作年限分类的员工，以及按公司分类的周年纪念日和工作年限 |
| 员工生日                               | 本月生日，下个月生日，员工生日，以及按月份和部门分类的生日 |
| 大批雇用项目                               | 大批雇用项目总计，按状态分类的大批雇用项目，按部门和所有者分类的大批雇用项目，按作业分类的大批雇用项目，以及大批雇用项目 |

可以筛选这些报表中的图表和磁贴，并将图表和磁贴固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。

请确保下载适用于您使用的 Microsoft Dynamics 365 版本的 **劳动力指标** Power BI 内容。

> [!NOTE]
> 在 Lifecycle Services 中可用的 .pbix 文件仅适用于 Finance and Operations 应用程序。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
下表显示内容所基于的实体。

| 实体                   | 内容                                                                            | 与其他实体之间的关系 |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| 日历偏差          | 要切分的日历偏差报表                                                   | 过去的职位分配、职位趋势、员工趋势、已离职的员工 |
| 公司                  | 充当报表筛选依据的公司                                                      | 当前员工、已离职的员工、员工趋势 |
| 当前职位         | 截至当前日期的职位，FTE，开放职位，以及待填补的职位 | 作业，职位 |
| 当前员工         | 截至当前日期的工作人员，年龄和人数                                  | 公司、地理位置、员工姓名、报告至、员工职务、人口统计学、作业、雇用、职位 |
| 日期                     | 天数、周数、月数和年数                                                      | 过去的职位分配、职位趋势、已离职的员工、员工趋势 |
| 人口统计数据             | 生日、性别、种族和婚姻状况                            | 当前员工、已离职的员工、员工趋势 |
| 雇用               | 开始日期、结束日期和转换日期                                           | 当前员工、已离职的员工、员工趋势 |
| 地理位置      | 市、县、邮政编码和省/市/自治区                                    | 当前员工、已离职的员工、员工趋势 |
| 作业                      | 功能，类型和标题                                                           | 当前职位、当前员工 |
| 过去的职位分配 | 分配原因，开始日期，结束日期和作业                                    | 日历偏差、日期、作业、职位 |
| 位置                 | 部门，FTE，职位，职位类型和标题                                 | 当前职位、当前员工 |
| 职位趋势           | 一段时间的职位，FTE 和工作                                                   | 日历偏差、日期、作业、职位 |
| 报告至               | 名字、姓氏和全名                                                | 当前员工、已离职的员工、员工趋势 |
| 已离职的员工      | 离休工作人员，离休日期，职务，职位和工作                      | 公司、地理位置、员工姓名、报告至、日历偏差、日期、员工职务、人口统计学、雇用、作业、职位 |
| 员工姓名            | 名字、姓氏和全名                                                | 当前工作人员、已离职的员工、员工趋势 |
| 员工职务           | 职务和资历日期                                                            | 当前员工、已离职的员工、员工趋势 |
| 员工趋势           | 一段时间的工作人员，人数，公司和职位                                 | 公司、地理位置、员工姓名、报告至、日历偏差、日期、员工职务、人口统计学、雇用、作业 |
| 大批雇用项目        | 大批雇用项目数量，项目所有者和项目状态                     | 公司，大批雇用行 |
| 大批雇用行           | 部门，雇用类型和职位                                           | 日期，作业，大批雇用项目 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]