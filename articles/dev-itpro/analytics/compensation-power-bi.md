---
title: "薪酬 Power BI 内容"
description: "此主题描述薪酬 Power BI 内容。 它说明如何访问报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: daf7232f13b5a2d4262a46f302bfd9e7efd60ead
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="compensation-power-bi-content"></a>薪酬 Power BI 内容

[!include[banner](../includes/banner.md)]

此主题描述**薪酬** Microsoft Power BI 内容。 它说明如何访问报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容
如果您使用以下其中一种产品，则**薪酬** Power BI 内容显示在**薪酬管理**工作区中：

- Microsoft Dynamics 365 for Finance and Operations Enterprise Edition（2017 年 7 月）
- Microsoft Dynamics 365 for Talent

## <a name="reports-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的报表
**薪酬** Power BI 内容中包含的报表有图表和表，其中包含更多信息。 下表对报表进行了描述。

| 报告                     | 内容 |
|----------------------------|----------|
| 薪酬概览      | 其他报表的汇总 |
| 薪酬分析      | 按公司分类的小时员工和固定员工，按薪酬计划分类的员工总数，按薪酬计划分类的男性员工和女性员工，以及按部门分类的员工薪酬 |
| 职位付薪分析      | 最高和最低的小时和工资付薪，最高和最低付薪的职位，以及全职和兼职职位 |
| 薪酬计划分析 | 按所选福利分类的员工登记 |

可以筛选这些报表中的图表和磁贴，并将图表和磁贴固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。

## <a name="extending-the-power-bi-content"></a>扩展 Power BI 内容
如果您使用的是 Microsoft Dynamics 365 for Operations 版本 1611 或 Finance and Operations Enterprise Edition（2017 年 7 月），您可以查找 LCS 共享资产库中的**薪酬** Power BI 内容。 有关如何下载内容并在您的组织中实现的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。 若要观看显示如何实现 Power BI 内容的演示，请参阅 [Dynamics Lifecycle Services 中来自 Microsoft 和您的合作伙伴的 Power BI 内容](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix。

请确保下载适用于您使用的 Microsoft Dynamics 365 版本的**薪酬** Power BI 内容。

>[!NOTE]
>在 Lifecycle Services 中可用的 .pbix 文件仅适用于 Finance and Operations。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
以下数据用于填充**薪酬** Power BI 内容中的报表。 此表显示内容所基于的实体。

| 实体                   | 内容                                                                                                   | 与其他实体之间的关系 |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| 日历偏差          | 要切分的日历偏差报表                                                                          | 过去的职位分配、职位趋势、员工趋势、已离职的员工 |
| 公司                  | 充当报表筛选依据的公司                                                                             | 当前薪酬、当前员工、已离职的员工、员工趋势 |
| 薪酬             | 一段时间的付薪比率和频率                                                                           | 当前薪酬、当前员工、已离职的员工、员工趋势 |
| 当前薪酬     | 截至当前日期的付薪比率和频率                                                              | 公司、薪酬、人口统计学、作业、职位 |
| 当前职位         | 截至当前日期的职位，全职等效 (FTE)，开放职位，以及待填补的职位 | 作业、职位 |
| 当前员工         | 截至当前日期的工作人员，年龄和人数                                                         | 公司、薪酬、地理位置、员工姓名、报告至、员工职务、人口统计学、作业、雇用、职位、福利 |
| 日期                     | 天数、周数、月数和年数                                                                             | 过去的职位分配、职位趋势、已离职的员工、员工趋势 |
| 人口统计数据             | 生日、性别、种族和婚姻状况                                                   | 当前员工、已离职的员工、员工趋势 |
| 雇用               | 开始日期、结束日期和转换日期                                                                  | 当前员工、已离职的员工、员工趋势 |
| 地理位置      | 市，县，邮政编码和省/市/自治区                                                           | 当前员工、已离职的员工、员工趋势 |
| 作业                      | 功能，类型和标题                                                                                  | 当前职位、当前员工 |
| 过去的职位分配 | 分配原因，开始日期，结束日期和作业                                                           | 日历偏差、日期、作业、职位 |
| 位置                 | 部门，FTE，职位，职位类型和标题                                                        | 当前职位、当前员工 |
| 职位趋势           | 一段时间的职位，FTE 和工作                                                                          | 日历偏差、日期、作业、职位 |
| 报告至               | 名字、姓氏和全名                                                                       | 当前工作人员、已离职的员工、员工趋势 |
| 已离职的员工      | 已离职的员工、离职日期、职务、职位和作业                                             | 公司、薪酬、地理位置、员工姓名、报告至、日历偏差、日期、员工职务、人口统计学、雇用、作业、职位、福利 |
| 福利                 | 生效日期，福利选项，福利计划和福利类型                                             | 当前姓名、已离职的员工、员工趋势 |
| 员工姓名            | 名字、姓氏和全名                                                                       | 当前员工、已离职的员工、员工趋势 |
| 员工职务           | 职务和资历日期                                                                                   | 当前员工、已离职的员工、员工趋势 |
| 员工趋势           | 一段时间的工作人员，人数，公司和职位                                                        | 公司、薪酬、地理位置、员工姓名、报告至、日历偏差、日期、员工职务、人口统计学、雇用、作业、福利 |

这些实体用于在数据模型中创建计算度量值。 然后，这些计算的度量值用于计算在内容中使用的关键绩效指标 (KPI) 和报表。 如果要在报表和仪表板中包含更多计算，可以从 LCS 下载 .pbix 文件并修改。 此文件是用于创建内容的默认数据模型。 修改后，可以创建包含您已添加的信息的组织内容包和仪表板。

