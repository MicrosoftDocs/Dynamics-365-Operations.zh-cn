---
title: 费用管理 Power BI 内容
description: 此主题介绍费用管理 Power BI 内容包中的内容。
author: panolte
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: aadf43d478eb4bf5af20df02dcc6399a7a2e71a5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743499"
---
# <a name="expense-management-power-bi-content"></a>费用管理 Power BI 内容

[!include [banner](../includes/banner.md)]

此主题介绍费用管理 Power BI 内容中的内容。 

## <a name="overview"></a>概览
有两个 Power BI 内容包可以与版本 8.1 及更高版本中的费用管理一起使用。 
- 有一个为提交费用报表的员工设计的个人仪表板。 

  该仪表板经过定制，可以向个人提供有关未提交金额和已提交金额的关键信息，以及历史记录和对费用交易记录历史记录的见解。 这个个人仪表板是一个页面，其中包含相应用户的最重要信息。

- 有一个为应付帐款职员和经理设计的管理员仪表板。 该仪表板针对全体员工费用的跟踪和报告进行过定制。 其中提供关键费用度量，如未提交的费用、里程和费用报表平均金额。 它使用交易记录数据，并且提供跨所有公司的费用管理的聚合视图。 还提供按员工的分解，以及用于添加财务维度数据的选项。 管理员费用分析内容中包含： 
  - 一个概览页面，其中包含有关费用金额的关键度量，以及对草稿、进行中和已完成费用报表的见解。 
  - 一个员工统计信息页面，用于按时间、成本类型和统计信息组查看有关员工的个人详细信息。 
  - 一个员工比较页面，用于比较一段时间的多个员工。 

所有金额均以公司币种显示。 将显示所有公司的数据，但是如果需要，可以添加公司筛选器。 

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容
可以在 Microsoft Dynamics Lifecycle Services (LCS) 中的共享资产库内找到 Expense Admin Dashboard.pbix 和 Expense Personal Dashboard.pbix Power BI 内容。 有关如何下载内容并在您的组织中实现的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/)。
该内容可以以嵌入式 Power Bi 内容的形式从费用管理工作区获取。 费用负责人可以访问自己的个人费用，但是只有应付帐款职员和经理可以访问管理员内容以查看所有用户的费用数据。

## <a name="refreshing-the-power-bi-content"></a>刷新 Power BI 内容
费用管理 Power BI 内容要求从实体商店刷新 TrvBiExpenseMeasurement 度量和 BudgetActivityMeasure。 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的度量
此内容中包含一组报表页面。 每个页面中包含一组可视化为图表、磁贴和表的指标。 下表概要介绍 Power BI 内容中的可视化项。

**个人费用分析**

| 报表页 | 可视化                             |
|-------------|-------------------------------------------|
| 我的支出 | 里程金额                         |
|             | 进行中费用报表                |
|             | 编号 未提交的费用               |
|             | 要支付的个人费用              |
|             | 未提交的金额                        |
|             | 已提交的金额                          |
|             | 待偿还金额             |
|             | 包含金额和状态的费用报表   |
|             | 已提交但未审核的费用报表  |
|             | 按成本类型的费用                     |
|             | 按商家的费用                      |
|             | 按已处理费用的费用            |
|             | 按项目的费用                       |
|             | 一段时间的交易记录总金额        |

**管理费用分析**

| 报表页         | 可视化                           |           
|---------------------|-----------------------------------------|
| 费用概览    | 草稿费用金额                   |
|                     | 草稿费用行数           |
|                     | 草稿费用行                     |
|                     | 费用报表策略违规        |
|                     | 未清金额                      |
|                     | 已提交但未审核的费用       |
|                     | 已审核的费用                       |
|                     | 支出总金额                    |
|                     | 费用报表汇总                |
|                     | 按成本类型的费用                   |
|                     | 按商家的费用                    |
|                     | 按员工的费用                   |
|                     | 费用与项目                     |
| 员工比较 | 费用金额                         |
|                     | 一段时间按员工的费用金额   |
| 员工统计信息 | 按成本类型的费用报表            |
|                     | 个人支出                       |
|                     | 按统计信息组的费用报表     |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]