---
title: "成本管理 Power BI 内容"
description: "此主题介绍成本管理 Power BI 内容中的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fb5c39a65ea59acda05b0828f84bfaea4ad75062
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="cost-management-power-bi-content"></a>成本管理 Power BI 内容

[!include[banner](../includes/banner.md)]


此主题介绍成本管理 Power BI 内容中的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。

# <a name="overview"></a>概览

**成本管理** Microsoft Power BI 内容适用于组织中的库存会计师或负责库存的个人。 **成本管理** Power BI 内容提供对库存和在制品 (WIP) 库存的管理洞察，并按类别介绍一段时间内成本在这些库存中的流向。 也可以将此信息用作财务报表的详细补充。

## <a name="key-measures"></a>关键度量

+ 期初余额
+ 期末余额
+ 净改变
+ 净更改（百分比）
+ 帐龄

## <a name="key-performance-indicators"></a>关键绩效指标
+ 库存周转
+ 库存准确性

CostAggregatedCostStatementEntryEntity 的主要数据源为 CostStatementCache 表。 此表由数据集高速缓存框架管理。 默认情况下，此表每隔 24 小时更新一次，但是您可以在数据高速缓存配置中启用手动更新。 可以在**成本管理**或**成本分析**工作区中执行手动更新。 运行 CostStatementCache 的更新之后，必须在 Power BI.com 中更新 OData 连接才能在该网址中查看更新后的数据。 此 Power BI 内容中的差异（采购、生产）度量仅适用于通过标准成本库存方法估值的物料。 生产差异计算为有效成本与实际成本之差。 生产订单的状态为**已结束**时，计算生产差异。 有关生产差异类型和如何计算各种类型的详细信息，请参阅[关于分析已完成生产订单的差异](https://technet.microsoft.com/en-us/library/gg242850.aspx)。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容
**成本管理** Power BI 内容可从 PowerBI.com 获取。有关如何连接和加载您的 Microsoft Dynamics 365 for Finance and Operations 数据的详细信息，请参阅[从 PowerBI.com 访问 Power BI 内容](power-bi-home-page.md)。

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的指标
此内容中包含一组报表页面。 每个页面中包含一组可视化为图表、磁贴和表的指标。 下表概要介绍**成本管理** Power BI 内容中的可视化。

| 报表页 | 图表 | 职称 |
|---|---|---|
|库存总体情况（默认按当前期间） |准确性 |库存度量：<br>库存期末余额<br>库存净更改<br>库存净更改百分比<br>|
| |库存周转 | |
| |按资源组的库存期末余额 | |
| |按类别名称级别 1 和类别名称级别 2 的库存净更改| |
| |按资源组和类别名称级别 3 的采购差异 | |
|按站点的库存（默认按当前期间） |按站点名称和资源组的库存期末余额 | |
| |按站点名称和资源组的库存周转 | |
| |按市/县和资源组的库存期末余额 | |
|按资源组的库存（默认按当前期间） |库存度量 | |
| |按金额和资源组的库存精确性 | |
| |按金额和资源组的库存周转 | |
|库存 YOY（默认本年对比上一年） |库存度量 | |
| |库存 KPI：<br>库存周转<br>库存准确性 | |
| |按年和资源组的库存期末余额 | |
| |按年和类别名称级别 3 的采购差异 | |
|库存帐龄（默认按本年） |按季度和资源组的库存帐龄 | |
| |按季度和站点名称的库存帐龄 | |
|WIP 总体情况（默认按当前期间） |按类别名称级别 1 和类别名称级别 2 的 WIP 净更改 |在制品 WIP 度量：<br>WIP 期末余额<br>WIP 净改变<br>WIP 净改变百分比<br> |
| |按资源组和类别名称级别 3 的生产差异 | |
| |按资源组的 WIP 净改变 | |
|按站点的 WIP（默认按当前期间） |在制品 WIP 度量 | |
| |按站点名称和类别名称级别 2 的 WIP 净更改 | |
| |按站点名称和类别名称级别 3 的生产差异 | |

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
Finance and Operations 数据用于填充**成本管理** Power BI 内容中的报表页面。 这些数据表示为实体商店（这是针对分析进行了优化的 Microsoft SQL 数据库）中暂存的聚合度量。 有关详细信息，请参阅 [Power BI 与实体商店集成概览](power-bi-integration-entity-store.md)。 以下关键聚合度量用作该内容的基础。

| 实体            | 关键聚合度量 | Finance and Operations 的数据源 | 字段             | 说明                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| 报表条目 | 净改变                | CostAggregatedCostStatementEntryEntity      | sum(\[Amount\])   | 按记帐币种计算的金额 |
| 报表条目 | 净更改数量       | CostAggregatedCostStatementEntryEntity      | sum(\[Quantity\]) |                                   |

下表显示如何使用关键聚合度量在该内容的数据集中创建若干计算度量。

| 度量                                 | 该度量的计算方法                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 期初余额                       | \[期末余额\]-\[净更改\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 期初余额数量              | \[期末余额数量\]-\[净更改数量\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 期末余额                          | CALCULATE(SUM(\[Amount\]), FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &lt;= MAX('Fiscal calendars'\[Date\])))                                                                                                                                                                                           |
| 期末余额数量                 | CALCULATE(SUM(\[Quantity\]), FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &lt;= MAX('Fiscal calendars'\[Date\])))                                                                                                                                                                                         |
| 库存期初余额             | CALCULATE(\[Beginning balance\], 'Statement entries'\[Statement Type\] = "Inventory")                                                                                                                                                                                                                                                                                                                                                                                      |
| 库存期末余额                | CALCULATE(\[Ending balance\], 'Statement entries'\[Statement Type\] = "Inventory")                                                                                                                                                                                                                                                                                                                                                                                         |
| 库存净更改                    | CALCULATE(\[Net change\], 'Statement entries'\[Statement type\] = "Inventory")                                                                                                                                                                                                                                                                                                                                                                                             |
| 库存净更改数量           | CALCULATE(\[Net change quantity\], 'Statement entries'\[Statement type\] = "Inventory")                                                                                                                                                                                                                                                                                                                                                                                    |
| 库存净更改百分比                  | IF(\[Inventory ending balance\] = 0, 0, \[Inventory net change\] / \[Inventory ending balance\])                                                                                                                                                                                                                                                                                                                                                                           |
| 按金额的库存周转                | if(OR(\[Inventory average balance\] &lt;= 0, \[Inventory sold or consumed issues\] &gt;= 0), 0, ABS(\[Inventory sold or consumed issues\])/\[Inventory average balance\])                                                                                                                                                                                                                                                                                                  |
| 库存平均余额               | (\[库存期末余额\] + \[库存期初余额\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| 已售或已消耗库存问题       | \[已售库存\] + \[库存的消耗物料成本\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 库存消耗的物料成本        | CALCULATE(\[Inventory net change\], 'Statement entries'\[Category name - level 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| 已售库存                          | CALCULATE(\[Inventory net change\], 'Statement entries'\[Category name - level 2\_\] = "Sold")                                                                                                                                                                                                                                                                                                                                                                             |
| 按金额的库存准确性            | IF(\[Inventory ending balance\] &lt;= 0, IF(OR(\[Inventory counted amount\] &lt;&gt; 0, \[Inventory ending balance\] &lt; 0), 0, 1), MAX(0, (\[Inventory ending balance\] - ABS(\[Inventory counted amount\]))/\[Inventory ending balance\]))                                                                                                                                                                                                                              |
| 库存盘点金额                | CALCULATE(\[Inventory net change\], 'Statement entries'\[Category name - level 3\_\] = "Counting")                                                                                                                                                                                                                                                                                                                                                                         |
| 库龄                         | if(ISBLANK(max('Fiscal calendars'\[Date\])), blank(), MAX(0, MIN(\[Inventory aging receipts quantity\], \[Inventory aging ending balance quantity\] - \[Inventory aging receipts quantity in the future\]))) \* \[Inventory avg unit cost\]                                                                                                                                                                                                                                |
| 库存帐龄收货数量       | IF(\[minDate\] = \[minDateAllSelected\], CALCULATE(\[Inventory net change quantity\], 'Statement entries'\[Quantity\] &gt; 0, FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &lt;= MAX('Fiscal calendars'\[Date\]))), CALCULATE(\[Inventory net change quantity\], 'Statement entries'\[Quantity\] &gt; 0)) |
| 库存帐龄期末余额数量 | \[Inventory ending balance quantity\] + CALCULATE(\[Inventory net change quantity\], FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &gt; max('Fiscal calendars'\[Date\]) ))                                                                                                                                 |
| 将来的库存帐龄收货  | CALCULATE(\[Inventory net change\], 'Statement entries'\[Amount\] &gt; 0, FILTER(ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]), 'Fiscal calendars'\[Date\] &gt; MAX('Fiscal calendars'\[Date\])))                                                                                                                                             |
| 库存平均单位成本                 | CALCULATE(\[Inventory ending balance\] / \[Inventory ending balance quantity\],ALLEXCEPT('Fiscal calendars', 'Fiscal calendars'\[LedgerRecId\], 'entities'\[ID\], 'entities'\[Name\], 'Ledgers'\[Currency\], 'Ledgers'\[Description\], 'Ledgers'\[Name\]))                                                                                                                                                                                                                 |
| 采购差异                      | CALCULATE(SUM(\[Amount\]), 'Statement entries'\[Category name - level 2\_\] = "Procured", 'Statement entries'\[Statement type\] = "Variance")                                                                                                                                                                                                                                                                                                                              |
| WIP 期初余额                   | CALCULATE(\[Beginning balance\], 'Statement entries'\[Statement Type\] = "WIP")                                                                                                                                                                                                                                                                                                                                                                                            |
| WIP 期末余额                      | CALCULATE(\[Ending balance\], 'Statement entries'\[Statement Type\] = "WIP")                                                                                                                                                                                                                                                                                                                                                                                               |
| WIP 净更改                          | CALCULATE(\[Net change\], 'Statement entries'\[Statement type\] = "WIP")                                                                                                                                                                                                                                                                                                                                                                                                   |
| WIP 净改变百分比                        | IF(\[WIP ending balance\] = 0, 0, \[WIP net change\] / \[WIP ending balance\])                                                                                                                                                                                                                                                                                                                                                                                             |
| 生产差异                    | CALCULATE(SUM(\[Amount\]), 'Statement entries'\[Category name - level 2\_\] = "ManufacturedCost", 'Statement entries'\[Statement type\] = "Variance")                                                                                                                                                                                                                                                                                                                      |
| 类别名称 - 级别 1                 | switch(\[Category name - level 1\_\], "None", "None", "NetSourcing", "Net sourcing", "NetUsage", "Net usage", "NetConversionCost", "Net conversion cost", "NetCostOfGoodsManufactured", "Net cost of goods manufactured", "BeginningBalance", "Beginning balance")                                                                                                                                                                                                         |
| 类别名称 - 级别 2                 | switch(\[Category name - level 2\_\], "None", "None", "Procured", "Procured", "Disposed", "Disposed", "Transferred", "Transferred", "Sold", "Sold", "ConsumedMaterialsCost", "Consumed material cost", "ConsumedManufacturingCost", "Consumed manufacturing cost", "ConsumedOutsourcingCost", "Consumed outsourcing cost", "ConsumedIndirectCost", "Consumed indirect cost", "ManufacturedCost", "Manufactured cost", "Variances", "Variances")                            |
| 类别名称 - 级别 3                 | switch(\[Category name - level 3\_\], "None", "None", "Counting", "None", "ProductionPriceVariance", "Production price", "QuantityVariance", "Quantity", "SubstitutionVariance", "Substitution", "ScrapVariance", "Scrap", "LotSizeVariance", "Lot size", "RevaluationVariance", "Revaluation", "PurchasePriceVariance", "Purchase price", "CostChangeVariance", "Cost change", "RoundingVariance", "Rounding variance")                                                   |

以下关键维度用作筛选器以切分聚合度量，以便获得粒度更细微，更深入的分析洞察。

| 实体           | 属性示例                       |
|------------------|----------------------------------------------|
| 实体         | ID，名称                                     |
| 会计日历 | 日历，月，期间，季度，年       |
| KPI 目标        | 库存精确性目标，库存周转目标 |
| 分类帐          | 货币，名称，描述                  |
| 站点            | ID，名称，国家/地区，市/县                      |

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](..\data-entities\data-entities.md)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](configure-power-bi-integration.md)





