---
title: 成本管理 Power BI 内容
description: 此主题介绍成本管理 Power BI 内容中的内容。
author: ShylaThompson
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, CostObjectWithLowestAccuracy, CostVarianceChart, CostObjectWithLowestTurn
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38f499a18e6757c60755a91ba62937350ef7550a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564884"
---
# <a name="cost-management-power-bi-content"></a>成本管理 Power BI 内容

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>概览

**成本管理** Microsoft Power BI 内容面向库存核算师或组织中负责库存或在制品 (WIP) 的状态或对此类状态感兴趣的个人，或负责分析标准成本差异或对此类差异感兴趣的人员。

> [!NOTE]
> 本主题中介绍的 **成本管理** Power BI 内容适用于 Dynamics 365 Finance and Operations 8.0。
> 
> 已废弃了 AppSource 站点中的 **成本管理** Power BI 内容包。 有关此项废弃的详细信息，请参阅 [Finance and Operations 的移除或弃用功能](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource)。

此 Power BI 内容提供分类格式，帮助您监控库存性能，并显示库存中的成本分布。 您可获取管理见解，如周转率、现货库存天数，以及首选聚合级别的“ABC 分类”（公司、物料、物料组或站点）。 也可以将可用信息用作财务报表的详细补充。

此 Power BI 内容基于 **CostObjectStatementCacheMonthly** 聚合度量构建，后者采用 **CostObjectStatementCache** 表充当主要数据源。 此表由数据集高速缓存框架管理。 默认情况下，此表每隔 24 小时更新一次，但是您可以在数据集高速缓存配置中更改更新频率或启用手动更新。 可以在 **成本管理** 工作区或 **成本分析** 工作区中运行手动更新。

每次更新 **CostObjectStatementCache** 表之后，必须先更新 **CostObjectStatementCacheMonthly** 聚合度量，再更新 Power BI 可视化中的数据。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容

**成本管理** Power BI 内容在 **成本管理** 和 **成本分析** 工作区中显示。

**成本管理** 工作区中包含以下选项卡：

- **概述** – 此选项卡显示应用程序数据。
- **库存会计状态** – 此选项卡显示 Power BI 内容。
- **制造会计状态** – 此选项卡显示 Power BI 内容。

**成本分析** 工作区中包含以下选项卡：

- **概述** – 此选项卡显示应用程序数据。
- **库存会计分析** – 此选项卡显示 Power BI 内容。
- **制造会计分析** – 此选项卡显示 Power BI 内容。
- **标准成本差异分析** – 此选项卡显示 Power BI 内容。

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的报表表

**成本管理** Power BI 内容包括一组含有一组指标的报表页。 这些指标显示为图表、磁贴和表。 

下面的表概要介绍 **成本管理** Power BI 内容中的可视化。

### <a name="inventory-accounting-status"></a>库存会计状态

| 报表页                               | 可视化                                   |
|-------------------------------------------|-------------------------------------------------|
| 库存概览                        | 期初余额                               |
|                                           | 净改变                                      |
|                                           | 净改变百分比                                    |
|                                           | 期末余额                                  |
|                                           | 库存准确性                              |
|                                           | 库存周转率                        |
|                                           | 现货库存天数                          |
|                                           | 周期内的有效产品                        |
|                                           | 周期内的有效成本对象                   |
|                                           | 按物料组分类的余额                           |
|                                           | 按站点分类的余额                                 |
|                                           | 按类别分类的报表                           |
|                                           | 按季度分类的净改变                           |
| 按站点和物料组分类的库存概览 | 按站点分类的库存准确性                      |
|                                           | 按站点分类的库存周转率                |
|                                           | 按站点分类的库存期末余额                |
|                                           | 按物料组分类的库存准确性                |
|                                           | 按物料组分类的库存周转率          |
|                                           | 按站点和物料组分类的库存期末余额 |
| 库存报表                       | 库存报表                             |
| 按站点分类的库存报表               | 按站点分类的库存报表                     |
| 按产品层次结构分类的库存报表  | 库存报表                             |
| 按产品层次结构分类的库存报表  | 按站点分类的库存报表                     |

### <a name="manufacturing-accounting-status"></a>制造会计状态

| 报表页                | 可视化                       |
|----------------------------|-------------------------------------|
| 年初至今的 WIP 概览           | 期初余额                   |
|                            | 净改变                          |
|                            | 净改变百分比                        |
|                            | 期末余额                      |
|                            | WIP 周转率                  |
|                            | WIP 现货天数                    |
|                            | 周期内的有效成本对象        |
|                            | 按资源组分类的净改变        |
|                            | 按站点分类的余额                     |
|                            | 按类别分类的报表               |
|                            | 按季度分类的净改变               |
| WIP statement / WIP 报表              | 期初余额                   |
|                            | 期末余额                      |
|                            | 按类别分类的 WIP 报表           |
| 按站点分类的 WIP 报表      | 期初余额                   |
|                            | 期末余额                      |
|                            | 按类别和站点分类的 WIP 报表  |
| 按层次结构分类的 WIP 报表 | 期初余额                   |
|                            | 期末余额                      |
|                            | 按类别层次结构分类的 WIP 报表 |

### <a name="inventory-accounting-analysis"></a>库存会计分析

| 报表页        | 可视化                                                                |
|--------------------|------------------------------------------------------------------------------|
| 库存详细信息  | 按期末余额分类的前 10 项资源                                           |
|                    | 按净改变增加前 10 项资源                                      |
|                    | 按净改变减小前 10 项资源                                      |
|                    | 按库存周转率分类的前 10 项资源                                 |
|                    | 按库存周转率和高于阈值的期末余额分类的资源 |
|                    | 按低准确性分类的前 10 项资源                                             |
| ABC 分类 | 库存期末余额                                                     |
|                    | 已消耗的材料                                                            |
|                    | 已售(COGS)                                                                  |
| 趋势库存   | 库存期末余额                                                     |
|                    | 库存净更改                                                         |
|                    | 库存周转率                                                     |
|                    | 库存准确性                                                           |

### <a name="manufacturing-accounting-analysis"></a>制造会计分析

| 报表页 | 可视化      |
|-------------|--------------------|
| WIP 趋势  | WIP 期末余额 |
|             | WIP 净改变     |
|             | WIP 周转率 |

### <a name="std-cost-variance-analysis"></a>标准成本差异分析

| 报表页                             | 可视化                                        |
|-----------------------------------------|------------------------------------------------------|
| 年初至今的采购价差异（标准成本） | 已采购余额                                     |
|                                         | 采购价差异                              |
|                                         | 采购价差异率                        |
|                                         | 按物料组分类的差异                               |
|                                         | 按站点分类的差异                                     |
|                                         | 按季节分类的采购价                            |
|                                         | 按季节和物料组分类的采购价             |
|                                         | 按不利采购价率分类的前 10 项资源 |
|                                         | 按有利采购价率分类的前 10 项资源   |
| 年初至今的生产差异（标准成本）     | 制造成本                                    |
|                                         | 生产差异                                  |
|                                         | 生产差异率                            |
|                                         | 按物料组分类的差异                               |
|                                         | 按站点分类的差异                                     |
|                                         | 按季节分类的生产差异                       |
|                                         | 按季节和差异类型分类的生产差异     |
|                                         | 按不利生产差异分类的前 10 项资源  |
|                                         | 按有利生产差异分类的前 10 项资源    |

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体

将使用来自应用程序的数据填充 **成本管理** Power BI 内容中的报表页。 这些数据表示为实体商店（这是针对分析进行了优化的 Microsoft SQL Server 数据库）中暂存的聚合度量。 有关详细信息，请参阅 [Power BI 与实体商店集成](power-bi-integration-entity-store.md)。

以下对象的关键聚合度量用作 Power BI 内容的基础。

| 对象                          | 关键聚合度量 | Finance and Operations 的数据源 | 字段               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | 时长                     | CostObjectStatementCache               | 时长              |
| CostObjectStatementCacheMonthly | 数量                   | CostObjectStatementCache               | 数量                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

下表显示 Power BI 内容中的关键计算度量。

| 度量                            | 计算 |
|------------------------------------|-------------|
| 期初余额                  | 期初余额 = \[期末余额\]-\[净改变\] |
| 期初余额数量             | 期初余额数量 = \[期末余额数量\]-\[净改变数量\] |
| 期末余额                     | 期末余额 = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))) |
| 期末余额数量                | 期末余额数量 = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))) |
| 净改变                         | 净改变 = SUM(\[AMOUNT\]) |
| 净改变数量                    | 净改变数量 = SUM(\[QTY\]) |
| 按金额分类的库存周转率 | 按金额分类的库存周转率 = if(OR(\[Inventory average balance\] \<= 0, \[Inventory sold or consumed issues\] \>= 0), 0, ABS(\[Inventory sold or consumed issues\])/\[Inventory average balance\]) |
| 库存平均余额          | 库存平均余额 = ((\[期末余额\] + \[期初余额\]) / 2) |
| 现货库存天数             | 现货库存天数 = 365 / CostObjectStatementEntries\[Inventory turnover ratio by amount\] |
| 库存准确性                 | 按金额的库存准确性 = IF(\[Ending balance\] \<= 0, IF(OR(\[Inventory counted amount\] \<\> 0, \[Ending balance\] \< 0), 0, 1), MAX(0, (\[Ending balance\] - ABS(\[Inventory counted amount\]))/\[Ending balance\])) |

以下关键维度用作筛选器以切分聚合度量，以便获得粒度更细微，更深入的分析洞察。


| 实体                                                  | 属性示例                          |
|---------------------------------------------------------|-------------------------------------------------|
| 产品                                                | 产品编号、产品名称、单位、物料组 |
| 类别层次结构（已分配给角色成本管理） | 类别层次结构，类别级别              |
| 法人                                          | 法人名称                              |
| 会计日历                                        | 会计日历、年、季度、期间、月   |
| 站点                                                    | ID、名称、地址、省/市/自治区、国家/地区               |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]