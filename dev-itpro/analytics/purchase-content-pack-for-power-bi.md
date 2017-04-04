---
title: "采购花费分析 Power BI 的内容"
description: "此主题描述在 Microsoft Power BI 的内容包采购花费分析中。 该说明如何访问在内容包包括的报表，并提供有关用于创建内容包的数据模型和实体的信息。"
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>采购花费分析 Power BI 的内容

此主题描述在 Microsoft Power BI 的内容包采购花费分析中。 该说明如何访问在内容包包括的报表，并提供有关用于创建内容包的数据模型和实体的信息。

<a name="overview"></a>概览
--------

Microsoft Power BI 的内容包采购花费分析为该负责采购预算经理和经理用于创建。 它用于帮助他们注视密切采购成本的。 为某工序使用从 Microsoft Dynamics 365 的采购交易记录数据，并按供应商和提供产品采购公司范围形象中的合计视图和采购成本细分。 在报表热点随着时间的推移花费的采购将更改。 因此，它们可用于告知有关正值和负值花费趋势的经理单独供应商和产品的。 图表显示不同的采购类别和供应商组的采购成本。 类别和地区经理可能会大有使用这些图表帮助标识在成本行为的变化。 内容包允许采购经理，并负责以下预算的方法：采购经理花费的分析

-   年初至今采购 (按供应商组和个体供应商、采购类别和产品和个体供应商位置)
-   连续多年的采购将更改 (按供应商组类别和采购)

## <a name="accessing-the-content-pack"></a>访问内容包
采购花费分析内容包在 Microsoft Dynamics Lifecycle Services (LCS) 过帐为实施资产，可以来自运营的 Microsoft Dynamics (LCS) 访问。 有关如何访问打开和 Power BI 报表的详细信息，请参阅在 [LCS 的 Power BI 的内容是从 Microsoft 和您的合作伙伴] (Microsoft partners.md BI 的内容。)

## <a name="metrics-that-are-included-in-the-content-pack"></a>在内容包包括的量化指标
采购花费分析内容包包括的度量。包含一组报表。 这些度量。为图表直观、平铺和表。 下表显示在内容包的可视化的概览。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>报表页面</th>
<th>图表</th>
<th>Tiles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>按供应商的采购</td>
<td><ul>
<li>按采购 (一堆方式条形图) 前 10 位的供应商</li>
<li>按供应商组/国家/地区名称 (饼图) 的总采购</li>
<li>按供应商组/国家/地区名称 (柱形图) 的采购</li>
<li>按供应商组/国家/地区名称 (柱形图) 的平均采购</li>
</ul></td>
<td><ul>
<li>采购总额</li>
<li>采购 YOY 增长</li>
<li>合计 # 供应商</li>
<li>合计 # 合作中供应商</li>
</ul></td>
</tr>
<tr class="even">
<td>采购副产品</td>
<td><ul>
<li>按采购类别/产品名称 (柱形图) 的采购</li>
<li>按采购类别/产品名称 (饼图) 的总采购</li>
<li>按采购 (一堆方式条形图前 10 位) 的产品</li>
</ul></td>
<td><ul>
<li>合计 # 产品</li>
<li>合计的总可用产品百分比 # 产品</li>
<li>占 80% 的采购的产品编号</li>
</ul></td>
</tr>
<tr class="odd">
<td>按 period*的采购</td>
<td><ul>
<li>按采购表示将柱形图 (天数) 之前</li>
<li>累计 YOY 采购差异 (瀑布图表)</li>
<li>总采购 YOY 柱形图 (增加)</li>
<li>采购矩阵 (报表)</li>
</ul></td>
<td><ul>
<li>采购 YOY 增长</li>
<li>采购 YOY 增长。</li>
</ul></td>
</tr>
<tr class="even">
<td>按供应商采购的位置</td>
<td><ul>
<li>按城市的采购</li>
<li>采购 YOY 增长。</li>
<li>按国家/地区的采购</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>采购花费分析按时间排序</td>
<td><ul>
<li>按采购当前年度 (天/月线形图) 之前</li>
<li>当前采购和之前年度 (行和图表列)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>采购供应商显示的支出分析</td>
<td><ul>
<li>前 10 位的供应商采购的采购 (漏斗)</li>
<li>在增加的消耗的 YOY 前 10 位的供应商</li>
<li>具有减少的消耗的 YOY 前 10 位的供应商</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* 则采购和本年度学习和发展按采购类别

## <a name="data-model-and-entities"></a>数据模型和实体
工序数据的 Dynamics 365 用于报表在采购花费分析内容包。 此数据表示为实体商店阶段，这是 Microsoft SQL 数据库为逻辑分析方法优化的聚合量化指标。 实体有关商店的详细信息，请参阅商店 [与实体的 Power BI 集成 Dynamics 的 https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)] (博客过帐。 {{在此：in}}内容包的聚合度量是可用于采购采用 Microsoft Dynamics 2012 和 Microsoft Dynamics AX 365 R3 工序中为 2012 个部分聚合的度量。 若要阶段多维数据集的度量中聚合实体商店，必须使它们可以部署。 有关详细信息，请参阅为某阶段聚合度量的方法。实体商店 [与实体商店的 Power BI 集成 Dynamics 的 https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)] (博客过帐。 以下参数聚合度量直接从发票行中获取和实体使用，因为内容包的基础。

| 实体        | Key aggregate measurements | Dynamics 365 数据的源的工序 | 字段              | 说明                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| 发票行 | 采购                   | VendInvoiceTrans                            | 总计 (LineAmountMST) | 以记帐币种计算的金额 |

下表显示在从实体发票行的内容包计算的关键度量。

| 度量               | 计算                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| 采购当前年度 | 采购合计“当前年度= (发票 lines'entity_PLACEHOLDER \ [采购\])                                            |
| 则采购    | 则采购计算总计 (“= (发票 lines'entity_PLACEHOLDER \ [采购\])，SAMEPERIODLASTYEAR (日期\[日期\])) |
| 采购 YOY 增长   | 采购 YOY 增长= \[采购当前年度\] –则 \[采购\]                            |

在内容包的以下关键度量维度用作切聚合的筛选器，这样，您可以获得详细精细程度和更深入的见解分析。

| 实体                 | 属性的示例                                |
|------------------------|-------------------------------------------------------|
| 供应商                | 供应商组、供应商国家或地区，供应商名称。 |
| 产品               | 产品编号，产品名称，物料组名称        |
| 采购类别 | 采购类别，采购类别名称      |
| 法人         | 法人姓名                                     |
| 日期                  | 日期，年度的偏移                                    |

默认情况下，显示内容包数据当前日历年度。 但是，您可以更改在报表部分日期筛选的筛选器。 您还可以更改公司筛选器。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](..\data-entities\data-entities.md)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](configure-power-bi-integration.md)



