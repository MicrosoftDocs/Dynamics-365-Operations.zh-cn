---
title: "成本核算分析 Power BI 内容"
description: "此主题介绍成本核算分析 Power BI 内容中的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: AndersGirke
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 2d0fb4de84838f1778625d977bdd2ceeaac61f8c
ms.contentlocale: zh-cn
ms.lasthandoff: 12/18/2017

---

# <a name="cost-accounting-analysis-power-bi-content"></a>成本核算分析 Power BI 内容

[!INCLUDE [banner](../includes/banner.md)]

此主题介绍**成本核算分析** Microsoft Power BI 内容中的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="overview"></a>概览

**成本核算分析** Power BI 内容面向成本总监或负责执行组织的成本控制的任何人。 其中包含关键指标，如成本、度量值，以及按实际成本、预算成本和可变预算成本的成本率。 它使用来自**成本核算**模块中的交易记录数据，并使用一种申报币种提供整个组织的成本聚合视图。 经理可以按成本对象筛选这些数据，以便对其组织单元执行成本控制，即使该组织有多个法人。 

由于**成本核算分析**内容突出显示实际成本与预算成本之间的差异，所以可以通知经理有关其运营单位正负趋势的信息。 经理可以向下钻取到成本元素层次结构或单独的成本元素。 这样，经理可详细了解成本差异是如何发生的，并采取有效的行动。 

成本会计员可通过**成本核算分析**内容分析成本在整个组织的成本对象中的流向。 

若要了解有关成本核算的详细信息，请参阅[成本核算主页](../../financials/cost-accounting/cost-accounting-home-page.md)。 

通过在成本核算中定义访问级安全并将其与 Power BI 中的行级安全结合，可以授予所有成本对象所有者**成本核算分析** Power BI 内容的访问权限。 然后将根据成本核算中控制的访问级别筛选可视化中的所有数据。 若要了解有关访问级安全和行级安全的详细信息，请参阅[设置成本核算 Power BI 内容的安全](setup-security-cost-accounting-content-pack.md)。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容
Microsoft Dynamics Lifecycle Services (LCS) 中的共享资产库内包含**成本核算分析** Power BI。 有关如何下载内容并在您的组织中实现的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/)。 若要观看显示如何实现 Power BI 内容的演示，请参阅 [Dynamics Lifecycle Services 中来自 Microsoft 和您的合作伙伴的 Power BI 内容](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix。

请确保下载适用于您使用的 Microsoft Dynamics 365 版本的**成本核算分析**内容。

> [!NOTE]
> KB 4011327 是此 Power BI 内容的先决条件。 登录 LCS 之后，可以在此处 <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327> 访问 KB。

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的指标
此内容中包含一组报表页面。 每个页面中包含一组可视化为图表、磁贴和表的指标。 下表概要介绍**成本核算分析** Power BI 内容中的可视化。

| 报表页                      | 图表                                                                                                                         | 磁贴                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 按会计期间的成本控制    | 按成本元素层次结构的实际成本和预算成本                                                                   | 实际成本与预算成本                    |
|                                  | 按成本元素层次结构的预算差异                                                                               | 实际成本率与预算成本率          |
|                                  | 按成本元素排名前 10 位的预算差异（百分比）                                                                          | 实际度量值与预算度量值          |
| 按年初至今的成本控制     | 按日历年期间的实际成本和预算成本                                                                           | 实际成本与预算成本                    |
|                                  | 按日历年期间的预算差异                                                                                       | 实际成本率与预算成本率          |
|                                  | 按成本元素排名前 10 位的预算差异（百分比）                                                                          | 实际度量值与预算度量值          |
| 按会计年度的成本率         | 按成本行为的实际成本率                                                                                             | 实际成本率与预算成本率          |
|                                  | 按成本元素层次结构级别的实际成本率、预算成本率差异、预算成本率百分比和预算成本率 | 实际度量值与预算度量值          |
|                                  | 按成本元素层次结构的预算差异                                                                               |                                               |
|                                  | 按成本元素排名前 10 位的预算差异（百分比）                                                                          |                                               |
| 按会计期间的可变预算 | 按成本元素层次结构级别的实际成本、预算成本和可变预算成本                                             | 实际度量值与预算度量值          |
|                                  | 按成本元素层次结构的预算差异和可变预算差异                                                  | 实际成本与可变预算成本           |
|                                  | 按成本行为和成本元素层次结构的实际成本、预算成本和可变预算成本                                  | 实际成本率与可变预算成本率 |
| 按会计期间的成本报表  | 按成本元素层次结构级别和成本对象维度成员名称的实际成本                                             |                                               |
|                                  | 按成本对象维度成员名称和成本元素维度成员名称的实际成本                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
以下数据用于填充**成本核算分析** Power BI 内容中的报表页。 此数据表示为实体商店内已分组的聚合度量。 实体商店是针对分析进行优化的 Microsoft SQL Server 数据库。 有关详细信息，请参阅 [Power BI 与实体商店集成概览](power-bi-integration-entity-store.md)。 

以下关键聚合度量用作该内容的基础。

| 实体                  | 关键聚合度量 | Dynamics 365 的数据源      | 字段     | 说明                                        |
|-------------------------|---------------------------|-----------------------------------|-----------|----------------------------------------------------|
| 成本核算条目 | SUM(Amount)               | CAMDATAAggregatedCostEntry        | 本币金额    | 成本核算分类帐币种金额。 |
| 统计条目     | SUM(Magnitude)            | CAMDATAAggregatedStatisctialEntry | 度量值 |                                                    |

下表显示如何使用关键聚合度量在该内容的数据集中创建若干计算度量。

| 度量                                       | 该度量的计算方法                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| 实际成本                                   | CALCULATE('Cost accounting entries'\[Measure\], 'Transaction versions'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)            |
| 预算成本                                   | CALCULATE('Cost accounting entries'\[Measure\], 'Transaction versions'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)            |
| 预算成本差异                          | \[预算成本\] - \[实际成本\]                                                                                      |
| 预算差异百分比                    | IF(\[Budget cost\] = 0, blank(), \[Budget variance\] / \[Budget cost\])                                                |
| 实际度量值                              | CALCULATE('Statistical entries'\[FullMagnitude\], 'Transaction versions'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)          |
| 预算度量值                              | CALCULATE(\[FullMagnitude\], 'Transaction versions'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)                               |
| 统计预算差异                   | \[预算度量值\] - \[实际度量值\]                                                                            |
| 统计预算差异百分比        | IF(\[Budget magnitude\] = 0, blank(), \[Statistical budget variance\] / \[Budget magnitude\])                          |
| 实际成本率                              | IF(\[Actual magnitude\] = 0, BLANK(), \[Actual cost\] / \[Actual magnitude\])                                          |
| 预算成本率                              | IF(\[Budget magnitude\] = 0, BLANK(), \[Budget cost\] / \[Budget magnitude\])                                          |
| 预算成本率差异                     | \[预算成本率\] - \[实际成本率\]                                                                            |
| 预算成本率差异百分比          | IF(\[Budget cost\] = 0, blank(), \[Budget cost rate variance\] / \[Budget cost rate\])                                 |
| 固定预算成本                             | CALCULATE(\[Budget cost\], 'Cost accounting entries'\[COSTBEHAVIOR\] = 1)                                              |
| 可变预算成本                          | CALCULATE(\[Budget cost\], 'Cost accounting entries'\[COSTBEHAVIOR\] = 2)                                              |
| 固定可变预算成本                    | \[固定预算成本\]                                                                                                  |
| 可变预算成本                 | IF(\[Budget magnitude\] = 0, BLANK(), (\[Variable budget cost\] / \[Budget magnitude\]) \* \[Actual magnitude\])       |
| 可变预算成本                          | \[固定可变预算成本\] + \[可变预算成本\]                                                     |
| 可变预算差异                      | \[可变预算成本\] - \[实际成本\]                                                                             |
| 可变预算差异百分比           | IF(\[Flexible budget cost\] = 0, BLANK(), \[Flexible budget variance\] / \[Flexible budget cost\])                     |
| 可变预算成本率                     | IF(\[Actual magnitude\] = 0, BLANK(), \[Flexible budget cost\] / \[Actual magnitude\])                                 |
| 可变预算成本率差异            | \[可变预算成本率\] - \[实际成本率\]                                                                   |
| 可变预算成本率差异百分比 | IF(\[Flexible budget cost rate\] = 0, BLANK(), \[Flexible budget cost rate variance\] / \[Flexible budget cost rate\]) |

以下关键维度用作筛选器以切分聚合度量，以便获得粒度更细微，更深入的分析洞察。


|               实体               |                                                属性示例                                                |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
|      成本核算分类帐       |                                                成本核算分类帐                                                |
|         成本控制单元         |                                                成本控制单元名称                                                |
|      成本元素维度       |     成本元素维度名称、成本元素维度成员名称、成本元素维度成员描述      |
|       成本对象维度       |       成本对象维度名称、成本对象维度成员名称、成本对象维度成员描述        |
|       统计维度       |       统计维度名称、统计维度成员名称、统计维度成员描述        |
| 成本对象维度层次结构  |  成本对象维度层次结构名称、成本对象维度层次结构级别、成本对象维度层次结构树   |
| 成本元素维度层次结构 | 成本元素维度层次结构名称、成本元素维度层次结构级别、成本元素维度层次结构树 |
| 统计维度层次结构  |  统计维度层次结构名称、统计维度层次结构级别、统计维度层次结构树   |
|        交易记录版本        |                                                     版本名                                                     |
|          会计日历          |                                            日历、日历描述                                            |
|            会计年度            |                                                    日历年度                                                     |
|           会计期间           |                                                 日历年度期间                                                 |


