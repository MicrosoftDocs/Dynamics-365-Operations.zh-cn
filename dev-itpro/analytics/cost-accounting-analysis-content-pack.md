---
title: "成本核算分析 Power BI 的内容"
description: "此主题描述在成本核算分析 Power BI 内容中。 该说明如何访问用于创建内容的 Power BI 报表，并且提供有关数据模型和实体的信息。"
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 50e7bd92ee693f59fd013226aee22bd1a54c81e2
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>成本核算分析 Power BI 的内容

此主题描述在成本核算分析 Power BI 内容中。 该说明如何访问用于创建内容的 Power BI 报表，并且提供有关数据模型和实体的信息。

<a name="overview"></a>概览
--------

对于执行组织的成本控制负责的**成本核算分析** Microsoft Power BI 内容为成本的财务总监或人员使用。 它按实际成本、预算成本和可变预算成本包含关键度量。，例如费用、度量值和成本率。 已在 Microsoft Dynamics 在 365 中使用一申报币种通过成本核算的交易记录数据。工序为整个的组织提供成本的合计视图。 经理可由成本组进行筛选数据对象执行其组织单位成本控制，即使，组织可能具有多个法人。 **由于成本核算分析** Power BI 突出显示在物料实际成本和预算成本之间的差异，经理可以将通知有关其单位的操作正值和负值趋势。 经理可以深化到详细了解到成本差异如何发生，然后执行有效成本的措施要素层次结构或单独的成本要素。 **成本核算分析** Power BI 内容通过成本会计员成本分析如何人士的整个组织的成本对象。 若要了解有关成本核算，请参阅成本核算主页 [] (/dynamics365/operations/financials/cost 核算/成本核算-主 page.md)。 通过定义在成本核算安全和合并的访问级别。它在 Power BI 的行级别的安全，您可以访问所有成本对象的所有者。**成本核算分析** Power BI 的内容输入。 的"可视化的数据基于在成本核算中控制的访问级别将筛选。 若要了解有关安全访问级别和行级别安全性，请参阅物料的 [成本核算设置安全的 Power BI 的] (成本核算设置安全 pack.md 内容)。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 的内容
您在 Microsoft Dynamics Lifecycle Services (LCS) 可以找到**成本核算分析** Power BI 的内容。共享资产库中。 有关如何将它连接和下载内容的更多信息。您的运营有关的数据，请参阅 Dynamics 365 在 [LCS 的 Power BI 的内容是从 Microsoft 和您的合作伙伴] (Microsoft partners.md BI 的内容。) **注释：**是一 KB4011327 ** **的先决条件。**成本核算分析** Power BI 的内容。  在登录到 Lifecycle Services 后，您可以访问 KB 此处：<https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>。

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI 的内容包括在量化指标
内容包含一组报表页面。 每页包括为图表直观、平铺和一组表的度量。 以下表提供在**成本核算分析** Power BI 的可视化内容的概览。

| 报表页面                      | 图表                                                                                                                         | 磁贴                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 成本控制按会计期间之前    | 实际成本和预算成本。要素层次结构级别成本。                                                                   | 实际成本{{与：vs}}预算成本                    |
|                                  | 按成本要素预算差异的层次结构级别                                                                               | 实际成本率{{与：vs}}预算成本率          |
|                                  | 前 10 位 (用百分比表示) 按成本预算差异要素                                                                          | 实际度量值{{与：vs}}预算度量值          |
| 成本控制年初至今     | 日历年度期间所用的实际成本和预算                                                                           | 实际成本{{与：vs}}预算成本                    |
|                                  | 预算差异按日历年度的期间                                                                                       | 实际成本率{{与：vs}}预算成本率          |
|                                  | 前 10 位 (用百分比表示) 按成本预算差异要素                                                                          | 实际度量值{{与：vs}}预算度量值          |
| 按会计年度前成本率         | 由成本组的行为的实际成本率                                                                                             | 实际成本率{{与：vs}}预算成本率          |
|                                  | 实际成本的成本率，预算差异，预算成本率百分比和预算成本的成本率。要素层次结构级别 | 实际度量值{{与：vs}}预算度量值          |
|                                  | 按成本要素预算差异的层次结构级别                                                                               |                                               |
|                                  | 前 10 位 (用百分比表示) 按成本预算差异要素                                                                          |                                               |
| 可变预算按会计期间之前 | 实际成本，预算成本和可变预算成本。要素层次结构级别成本。                                             | 实际度量值{{与：vs}}预算度量值          |
|                                  | 预算差异和可变预算差异按成本要素层次结构级别                                                  | 实际成本{{与：vs}}可变预算成本           |
|                                  | 实际成本，预算成本和可变成本由成本组的行为和成本要素层次结构级别                                  | 实际成本率{{与：vs}}预算可变成本率 |
| 成本报表按会计期间之前  | 按成本要素层次结构成本对象级别和维度成员名称的实际成本                                             |                                               |
|                                  | 由成本组进行对象维度成员名称要素成本和维度成员名称的实际成本                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
工序数据的 Dynamics 365 用于填充在**成本核算分析** Power BI 内容的报表页面。 此数据表示为实体商店阶段，这是 Microsoft SQL 数据库为逻辑分析方法优化的聚合量化指标。 有关详细信息，请参阅 [Power BI 集成概览与实体商店] (BI 集成功能) 的 store.md 实体。 以下参数聚合量化指标时作为物料的基础。

| 实体                  | 关键度量合计 | Dynamics 365 数据的源的工序 | 字段     | 说明                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| 成本核算条目 | 总和 (金额)               | CAMDATAAggregatedCostEntry                  | 本币金额    | 成本核算的会计币种金额。 |
| 统计条目     | 总和 (度量值)            | CAMDATAAggregatedStatisctialEntry           | 度量值 |                                               |

下表显示如何聚合关键度量用于创建在内容的数据集的若干计算度量值。

| 度量                                       | 如何计算量化指标                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| 实际成本                                   | 计算 (“成本核算 entries'entity_PLACEHOLDER \ [度量\]，"交易记录 versions'entity_PLACEHOLDER \ ISSOURCEVERSIONBUDGET [\_值\] =\])            |
| 预算成本                                   | 计算 (“成本核算 entries'entity_PLACEHOLDER \ [度量\]，"交易记录 versions'entity_PLACEHOLDER \ ISSOURCEVERSIONBUDGET [\_值\] =\])            |
| 预算成本差异                          | \[预算成本的\] - \[entity_PLACEHOLDER\[\]成本\]                                                                                      |
| 预算差异百分比                    | 如果 (\[预算成本的\] = (\[，为空)，\[预算差异\] / \[entity_PLACEHOLDER\[预算成本\]entity_PLACEHOLDER\])                                                |
| 实际度量值                              | 计算 (‘统计 entries'entity_PLACEHOLDER \ FullMagnitude [\]，"交易记录 versions'entity_PLACEHOLDER \ ISSOURCEVERSIONBUDGET [\_值\] =\])          |
| 预算度量值                              | 计算 (\[FullMagnitude\]，"交易记录 versions'entity_PLACEHOLDER \ ISSOURCEVERSIONBUDGET [\_值\] =\[)                               |
| 统计预算差异                   | \[预算、维度值\] - \[entity_PLACEHOLDER\[实际\]值                                                                            |
| 统计预算差异百分比        | 如果 (\[预算、维度值\] =\[，为空)，\[统计 (预算差异\] / \[entity_PLACEHOLDER\[预算\]维度值 entity_PLACEHOLDER\])                          |
| 实际成本率                              | 如果 (\[实际度量值 (\] =\[，为空)，\[实际成本\] / \[实际 entity_PLACEHOLDER\[\]值 entity_PLACEHOLDER\])                                          |
| 预算成本率                              | 如果 (\[预算、维度值\] = (\[，为空)，\[预算成本的\] / \[entity_PLACEHOLDER\[预算\]维度值 entity_PLACEHOLDER\])                                          |
| 成本率预算差异                     | \[预算\]成本率 - \[entity_PLACEHOLDER\[实际成本率\]                                                                            |
| 成本率预算差异百分比          | 如果 (\[预算成本的\] =\[，为空)，\[成本率 (预算差异\] / \[entity_PLACEHOLDER\[预算\]entity_PLACEHOLDER\])                                 |
| 固定的预算成本                             | 计算 (\[预算成本的\]，" [COSTBEHAVIOR 成本核算 entries'entity_PLACEHOLDER \\] =\[)                                              |
| 可变预算的成本                          | 计算 (\[预算成本的\]，" [COSTBEHAVIOR 成本核算 entries'entity_PLACEHOLDER \\] =\[)                                              |
| 固定的可变预算成本                    | \[固定的预算成本\]                                                                                                  |
| 可变的可变预算成本                 | 如果 (\[预算、维度值\] = (\[，为空)，\[(可变预算的成本\]的 / \[entity_PLACEHOLDER\[预算\]维度值 entity_PLACEHOLDER\] \*\[entity_PLACEHOLDER\[实际度量值 entity_PLACEHOLDER\])       |
| 可变预算成本                          | \[维修可变预算的成本\] + \[entity_PLACEHOLDER\[可变的可变预算的成本\]                                                     |
| 可变预算差异                      | \[可变预算的成本\] - \[entity_PLACEHOLDER\[\]成本\]                                                                             |
| 可变预算差异百分比           | 如果 (\[可变预算的成本\] =\[，为空)，\[(可变预算差异\] / \[entity_PLACEHOLDER\[可变预算的\]entity_PLACEHOLDER\])                     |
| 预算可变成本率                     | 如果 (\[实际度量值\] =\[，为空)，\[(可变预算的成本\] / \[实际 entity_PLACEHOLDER\[\]值 entity_PLACEHOLDER\])                                 |
| 可变预算差异成本率            | \[可变预算\]成本率 - \[entity_PLACEHOLDER\[实际成本率\]                                                                   |
| 可变预算差异百分比成本率 | 如果 (\[预算可变成本率\] =\[，为空)，\[(可变预算差异\]成本率 / \[entity_PLACEHOLDER\[预算可变\]entity_PLACEHOLDER\]) |

以下关键度量维度用作切聚合的筛选器实现更佳的精细程度并提供更深入的见解分析。

| 实体                             | 属性的示例                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| 成本核算分类帐            | 成本核算分类帐                                                                                               |
| 成本控制单元                 | 成本控制单元名称                                                                                               |
| 成本元素维度            | 成本要素维度名称，成本要素维度成员名称，成本要素维度成员描述          |
| 成本对象维度             | 成本的对象维度名称，成本对象维度成员名称，成本对象描述维度成员              |
| 统计维度             | 统计维度名称，统计维度成员名称，成员描述维度统计              |
| 成本对象的维度层次结构  | 成本对象的维度层次结构，对象名称成本维度层次结构级别，成本对象树维度层次结构    |
| 成本要素维度层次结构 | 成本要素维度层次结构成本，名称要素维度层次结构级别成本要素，维度层次树结构 |
| 统计维度层次结构  | 统计维度层次结构名称，统计维度层次结构级别，统计维度层次树结构    |
| 交易记录版本               | 版本名                                                                                                         |
| 会计日历                   | 日历，日历描述                                                                                       |
| 会计年度                       | 日历年度                                                                                                        |
| 会计期间                     | 日历年度期间                                                                                                 |

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](..\data-entities\data-entities.md)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](configure-power-bi-integration.md)
-   [设置成本核算安全内容的 Power BI 的] (成本核算设置安全 pack.md 内容)


