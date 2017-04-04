---
title: "Power BI 的内容管理"
description: "此主题描述在成本管理 Power BI 的内容中。 该说明如何访问用于创建内容的 Power BI 报表，并且提供有关数据模型和实体的信息。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>Power BI 的内容管理

此主题描述在成本管理 Power BI 的内容中。 该说明如何访问用于创建内容的 Power BI 报表，并且提供有关数据模型和实体的信息。

# <a name="overview"></a>概览

**的成本管理** Microsoft Power BI 内容为负责库存的库存使用组织的会计或个体。 **成本管理** Power BI 的内容管理提供答案到库存和进行中的工作 (WIP)，库存，而成本如何按类别随着时间的推移当它们。 信息可能还作为详细补充。财务报表。

## <a name="key-measures"></a>关键度量

+ 期初余额
+ 期末余额
+ 净改变
+ 在" % "中的净改变
+ 帐龄

## <a name="key-performance-indicators"></a>关键绩效指标
+ 库存周转
+ 库存准确性

CostAggregatedCostStatementEntryEntity 数据的主要来源是 CostStatementCache 表。 下表按数据集缓存框架管理。 默认情况下，每 24 小时，更新表，但您可以在数据缓存配置中启用可以手动更新。 然后可以执行用于手动更新。**的成本或成本管理** **分析**工作区。 在 CostStatementCache 更新计算后，必须 BI.com 的更新在高级 OData 连接查看站点上的更新数据。 Power BI 的内容{{在此：in}}采购，生产差异 (度量) 仅与通过标准成本库存 valuated 方法的物料。 生产差异作为在计算有效成本和实际成本之间的差异。 在计算生产差异，生产订单具有状态时** **结束。 有关生产差异类型的详细信息和各类型如何计算，请参阅关于 [分析已完成生产订单的 https://technet.microsoft.com/en-us/library/gg242850.aspx)] (差异。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 的内容
**成本管理**的 Power BI 的内容是从 PowerBI.com 获取。 有关连接方式和加载您的工序数据的 Microsoft Dynamics 365 的详细信息，请参阅访问 PowerBI.com [] (从的主 page.md BI 的 Power BI 的内容。)

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI 的内容包括在量化指标
内容包含一组报表页面。 每页包括为图表直观、平铺和一组表的度量。 以下表提供在**成本管理**的 Power BI 的可视化内容的概览。

| 报表页面 | 图表 | 职称 |
|---|---|---|
|整个库存 (按当前默认期间前) |准确性 |库存维度：<br>库存期末余额<br>更改库存净额<br>库存净额更改。<br>|
| |库存周转 | |
| |按资源组的库存期末余额 | |
| |库存 (按类别名称级别 1 和类别 2 级名称更改的净额| |
| |采购差异按资源组和类别 3 级名称 | |
|按站点 (默认的库存按当前期间之前) |按站点名称和资源组的库存期末余额 | |
| |按站点名称和资源组的库存轮 | |
| |按城市和资源组的库存期末余额 | |
|库存按资源组 (按当前默认期间前) |库存维度。 | |
| |按金额的精确性库存按资源组 | |
| |按金额的库存轮按资源组 | |
|库存 YOY (默认当前年度{{与：vs}}以前年度) |库存维度。 | |
| |库存 KPI:<br>库存周转<br>库存准确性 | |
| |期末余额库存按年份和资源组之前 | |
| |按采购差异年度和类别 3 级名称 | |
|帐龄默认库存 (按当前年度前) |按季度和资源组的库存帐龄 | |
| |按季度和帐龄的库存站点名称 | |
|总 WIP (按当前默认期间前) |WIP 按类别名称级别 1 和类别 2 级名称更改的净额 |在制品 WIP 度量：<br>WIP 期末余额<br>WIP 净额更改<br>WIP 净额更改。<br> |
| |按资源组和类别名称的生产差异级别 3 | |
| |WIP 按资源组更改的净额 | |
|按站点 (默认的 WIP 期间前按当前) |在制品 WIP 度量 | |
| |WIP 按站点名称的净额更改和类别 2 级名称 | |
| |按站点名称和类别名称级别 3 的生产差异 | |

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
工序数据的 Dynamics 365:用于填充时，会在**成本管理** Power BI 的内容的报表页面。 此数据表示为实体商店阶段，这是 Microsoft SQL 数据库为逻辑分析方法优化的聚合量化指标。 有关详细信息，请参阅 [Power BI 集成概览与实体商店] (BI 集成功能) 的 store.md 实体。 以下参数聚合量化指标时作为物料的基础。

| 实体            | 关键度量合计 | Dynamics 365 数据的源的工序 | 字段             | 说明                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| 报表条目 | 净改变                | CostAggregatedCostStatementEntryEntity      | 总计 (\[金额\])   | 记帐币种金额。 |
| 报表条目 | 净数量更改       | CostAggregatedCostStatementEntryEntity      | 总计 (\[数量\]) |                                   |

下表显示如何聚合关键度量用于创建在内容的数据集的若干计算度量值。

| 度量                                 | 如何计算量化指标                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 期初余额                       | \[期末余额\]-\[净额更改\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 开始的余额数量              | \[期末余额\]数量-\[净额更改数量\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 期末余额                          | 计算 (\[金额之和 (\])，筛选器 (ALLEXCEPT (‘会计日历的会计 calendars'entity_PLACEHOLDER，" [LedgerRecId \\]，" [entities'entity_PLACEHOLDER \ ID\]，" [entities'entity_PLACEHOLDER \ \ Ledgers'entity_PLACEHOLDER 名称\]，" [币种\]，" [Ledgers'entity_PLACEHOLDER \ \ Ledgers'entity_PLACEHOLDER 描述\]，" [\]名称)，calendars'entity_PLACEHOLDER \“财务日期\]&lt;= [MAX (‘会计 calendars'entity_PLACEHOLDER \ [日期\])))                                                                                                                                                                                           |
| 期末余额数量                 | 计算 (总和 (\[数量)，\]筛选器 (ALLEXCEPT (‘会计日历的会计 calendars'entity_PLACEHOLDER，" [LedgerRecId \\]，" [entities'entity_PLACEHOLDER \ ID\]，" [entities'entity_PLACEHOLDER \ \ Ledgers'entity_PLACEHOLDER 名称\]，" [币种\]，" [Ledgers'entity_PLACEHOLDER \ \ Ledgers'entity_PLACEHOLDER 描述\]，" [\]名称)，calendars'entity_PLACEHOLDER \“财务日期\]&lt;= [MAX (‘会计 calendars'entity_PLACEHOLDER \ [日期\])))                                                                                                                                                                                         |
| 库存期初余额             | 计算 (\[期初余额\]，"报表 entries'entity_PLACEHOLDER \ [报表类型\] =“库存”)                                                                                                                                                                                                                                                                                                                                                                                      |
| 库存期末余额                | 计算 (\[期末余额\]，"报表 entries'entity_PLACEHOLDER \ [报表类型\] =“库存”)                                                                                                                                                                                                                                                                                                                                                                                         |
| 更改库存净额                    | 计算 (\[净额更改\]，"报表 entries'entity_PLACEHOLDER \ [报表类型\] =“库存”)                                                                                                                                                                                                                                                                                                                                                                                             |
| 净额更改库存数量           | 计算 (\[净额更改数量\]，"报表 entries'entity_PLACEHOLDER \ [报表类型\] =“库存”)                                                                                                                                                                                                                                                                                                                                                                                    |
| 库存净额更改。                  | 如果 (库存\[期末余额\] =\[，\]，\[净额更改库存\] / \[库存 entity_PLACEHOLDER\[期末余额 entity_PLACEHOLDER\])                                                                                                                                                                                                                                                                                                                                                                           |
| 轮的库存按金额                | 如果 ((或\[库存平均余额\]&lt;=\[，\[库存中的销售或使用的问题\]&gt;=\] )，0，招聘 (\[库存中的销售或使用的问题\])/\[库存平均余额\])                                                                                                                                                                                                                                                                                                  |
| 库存平均余额               | 库存 (\[期末余额\] + \[库存 entity_PLACEHOLDER\[期初余额 entity_PLACEHOLDER\]/\[)                                                                                                                                                                                                                                                                                                                                                                                                       |
| 库存中的销售或使用的问题       | \[库存销售\] + \[entity_PLACEHOLDER\[库存使用的材料成本\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 库存使用的材料成本        | 计算 (\[净额更改库存\]，"报表 entries'entity_PLACEHOLDER \ [类别名称-\_级别\[\] =“ConsumedMaterialsCost”)                                                                                                                                                                                                                                                                                                                                                            |
| 出售的库存                          | 计算 (\[净额更改库存\]，"报表 entries'entity_PLACEHOLDER \ [类别名称-\_级别\[\] =“销售”)                                                                                                                                                                                                                                                                                                                                                                             |
| 按金额的精确性库存            | 如果 (库存\[期末余额，\]&lt;=\[(或者，如果\[(库存盘点金额\]&lt;&gt;\]，\[库存期末余额\]&lt; 0))，\[，\]，0，\[MAX ((库存\] 招聘-期末余额 (\[库存盘点金额\])) 库存/\[期末余额\]))                                                                                                                                                                                                                              |
| 库存盘点金额                | 计算 (\[净额更改库存\]，"报表 entries'entity_PLACEHOLDER \ [类别名称-\_级别\[\] =“盘点”)                                                                                                                                                                                                                                                                                                                                                                         |
| 库龄                         | 如果 (最大的 ISBLANK (“会计 calendars'entity_PLACEHOLDER \ [日期\]))，留空 ()，MAX (0 分钟，库存 (\[帐龄收货数量\]，库存 \[帐龄期末余额\]数量 - \[库存 entity_PLACEHOLDER\[帐龄收货数量在将来 entity_PLACEHOLDER\]))) \* \[库存单位成本\]日期                                                                                                                                                                                                                                |
| 帐龄库存收货数量       | 如果 (\[minDate\] = \[entity_PLACEHOLDER\[\]entity_PLACEHOLDER\]，计算库存 entity_PLACEHOLDER\[\[净额更改\]entity_PLACEHOLDER\]，"报表 entries'entity_PLACEHOLDER \ [\[，\]&gt; entity_PLACEHOLDER\] 筛选器 (ALLEXCEPT (‘会计日历的会计 calendars'entity_PLACEHOLDER，" [\]\ entity_PLACEHOLDER\]，" [entities'entity_PLACEHOLDER \\]entity_PLACEHOLDER\]，" [entities'entity_PLACEHOLDER \ \ Ledgers'entity_PLACEHOLDER\]entity_PLACEHOLDER\]，" [\]entity_PLACEHOLDER\]，" [Ledgers'entity_PLACEHOLDER \ \ Ledgers'entity_PLACEHOLDER\]entity_PLACEHOLDER\]，" [entity_PLACEHOLDER\]\])，calendars'entity_PLACEHOLDER \ "财务\]&lt;entity_PLACEHOLDER\] = [MAX (‘会计 calendars'entity_PLACEHOLDER \ [\]entity_PLACEHOLDER\])))，计算库存\[(净额更改数量\]，"报表 entries'entity_PLACEHOLDER \ [数量\]&gt;\[)) |
| 帐龄期末余额库存数量 | 库存\[期末余额计算\] + 数量 (库存\[净额更改数量\]，筛选器 (ALLEXCEPT (‘会计日历的会计 calendars'entity_PLACEHOLDER，" [LedgerRecId \\]，" [entities'entity_PLACEHOLDER \ ID\]，" [entities'entity_PLACEHOLDER \ \ Ledgers'entity_PLACEHOLDER 名称\]，" [币种\]，" [Ledgers'entity_PLACEHOLDER \ \ Ledgers'entity_PLACEHOLDER 描述\]，" [\]) 名称，会计 calendars'entity_PLACEHOLDER \“[日期\] 最 &gt; 大\]“(财务 calendars'entity_PLACEHOLDER \ [日期\])))                                                                                                                                 |
| 帐龄在将来库存收货  | 计算 (\[净额更改库存\]，"报表 entries'entity_PLACEHOLDER \ [\[金额\]&gt;，筛选器 (ALLEXCEPT (‘会计日历的会计 calendars'entity_PLACEHOLDER，" [LedgerRecId \\]，" [entities'entity_PLACEHOLDER \ ID\]，" [entities'entity_PLACEHOLDER \ \ Ledgers'entity_PLACEHOLDER 名称\]，" [币种\]，" [Ledgers'entity_PLACEHOLDER \ \ Ledgers'entity_PLACEHOLDER 描述\]，" [\]) 名称，会计 calendars'entity_PLACEHOLDER \“[日期\]&gt; MAX (‘会计 calendars'entity_PLACEHOLDER \ [日期\])))                                                                                                                                             |
| 日期库存单位成本                 | 计算 (\[库存\]期末余额 / \[entity_PLACEHOLDER\[库存\]entity_PLACEHOLDER\] 期末余额，ALLEXCEPT (‘会计日历的、"会计 calendars'entity_PLACEHOLDER \\][entity_PLACEHOLDER\]，" [entities'entity_PLACEHOLDER \\]entity_PLACEHOLDER\]，" [entities'entity_PLACEHOLDER \ \ Ledgers'entity_PLACEHOLDER\]entity_PLACEHOLDER\]，" [\]entity_PLACEHOLDER\]，" [Ledgers'entity_PLACEHOLDER \ \ Ledgers'entity_PLACEHOLDER\]entity_PLACEHOLDER\]，" [entity_PLACEHOLDER\]\]))                                                                                                                                                                                                                 |
| 采购差异                      | 计算 (\[金额之和 (\])，"报表 entries'entity_PLACEHOLDER \ [类别名称-\_级别\[\] =“采购”，"报表 entries'entity_PLACEHOLDER \ [报表类型\] =“差额”)                                                                                                                                                                                                                                                                                                                              |
| WIP 期初余额                   | 计算 (\[期初余额\]，"报表 entries'entity_PLACEHOLDER \ [报表类型\] =“WIP”)                                                                                                                                                                                                                                                                                                                                                                                            |
| WIP 期末余额                      | 计算 (\[期末余额\]，"报表 entries'entity_PLACEHOLDER \ [报表类型\] =“WIP”)                                                                                                                                                                                                                                                                                                                                                                                               |
| WIP 净额更改                          | 计算 (\[净额更改\]，"报表 entries'entity_PLACEHOLDER \ [报表类型\] =“WIP”)                                                                                                                                                                                                                                                                                                                                                                                                   |
| WIP 净额更改。                        | 如果 (\[WIP 期末余额\] =\[，\]，\[WIP 净额更改\] / \[WIP entity_PLACEHOLDER\[期末余额 entity_PLACEHOLDER\])                                                                                                                                                                                                                                                                                                                                                                                             |
| 生产差异                    | 计算 (\[金额之和 (\])，"报表 entries'entity_PLACEHOLDER \ [类别名称-\_级别\[\] =“ManufacturedCost”，"报表 entries'entity_PLACEHOLDER \ [报表类型\] =“差额”)                                                                                                                                                                                                                                                                                                                      |
| 类别- 1 级名称                 | 切换 (\[类别名称-\_级别\[，\]“无“，“"“，“NetSourcing”净来源，“添加“，“NetUsage“，“净使用”“NetConversionCost，F，G 净加工成本“，“NetCostOfGoodsManufactured F，G 制造的净成本货物，”“”，BeginningBalance“开始”余额)                                                                                                                                                                                                         |
| 类别- 2 级名称                 | 切换 (\[类别名称-\_级别\[，\]“无“，“"“，“采购“，“采购“，“配置”，“配置“，“转移”，“转移”，“销售“，“销售“，“ConsumedMaterialsCost F，G 使用的材料成本“，“ConsumedManufacturingCost F，G 使用的制造成本“，“ConsumedOutsourcingCost F，G 使用的外包成本“，“ConsumedIndirectCost F，G 使用的间接成本“，“ManufacturedCost F，G 制造的费用 F，G 差异“，“差额”)                            |
| 类别- 3 级名称                 | 切换 (\[类别名称-\_级别\[，\]“无“，“"“，“盘点“，“"“，“ProductionPriceVariance F，G 生产价格，”“”，QuantityVariance“数量“，“SubstitutionVariance F，G 替换“，“ScrapVariance”报废，“”“，LotSizeVariance F，G 批次规模，”“”，RevaluationVariance“重新计算“，“PurchasePriceVariance F，G 采购价“，“CostChangeVariance F，G 成本变化，”“”，RoundingVariance“舍入差额”)                                                   |

以下关键度量维度用作切聚合的筛选器实现更佳的精细程度并提供更深入的见解分析。

| 实体           | 属性的示例                       |
|------------------|----------------------------------------------|
| 实体         | ID，名称                                     |
| 会计日历 | 日历，图中，期间，季度，年度       |
| KPI 目标        | 库存精确性目标，库存轮目标 |
| 分类帐          | 币种，名称，描述                  |
| 站点            | ID，名称，则"国家/地区"，将填入城市                      |

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](..\data-entities\data-entities.md)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](configure-power-bi-integration.md)



