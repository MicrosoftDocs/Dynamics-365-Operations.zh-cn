---
title: "采购支出分析 Power BI 内容"
description: "此主题描述 Microsoft Power BI 的采购支出分析内容包中的内容。 它说明如何访问内容包中包括的报表，并提供有关用于构建内容包的数据模型和实体的信息。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ad0ee95113d05710cccc1a5e9d215b38244c2047
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>采购支出分析 Power BI 内容

[!include[banner](../includes/banner.md)]


此主题描述 Microsoft Power BI 的采购支出分析内容包中的内容。 它说明如何访问内容包中包括的报表，并提供有关用于构建内容包的数据模型和实体的信息。

<a name="overview"></a>概览
--------

Microsoft Power BI 的采购支出分析内容包是为采购经理和负责预算的经理创建的。 它用于帮助他们密切关注采购支出。 它使用来自 Microsoft Dynamics 365 for Operations 的采购交易数据，并且同时提供公司范围的采购数据聚合视图和按供应商与产品分类的采购支出分解。 报表突出显示一段时间的采购支出变化。 因此，可将其用于提醒经理有关单个供应商和产品的正负支出趋势的信息。 图表显示不同采购类别和供应商组的采购支出。 目录和区域经理可能发现这些图表非常有用，可用于帮助识别支出行为的变化。 采购经理和负责预算的经理可使用此内容包按照以下方式分析采购支出：

-   本年迄今的采购（按供应商组和单个供应商、采购类别和单个产品，以及供应商位置）
-   各年的采购变化（按供应商组和采购类别）

## <a name="accessing-the-content-pack"></a>访问内容包
“采购支出分析”内容包发布为 Microsoft Dynamics Lifecycle Services (LCS) 中的实施资产，并且可以从 Microsoft Dynamics 365 for Operations 访问。 有关如何访问和打开 Power BI 报表的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。
注意：KB 4011327 是此 Power BI 内容的先决条件。 登录 Lifecycle Services 之后，可以在以下位置访问该 KB：https://fix.lcs.dynamics.com/issue/results/?q=kb4011327。

## <a name="metrics-that-are-included-in-the-content-pack"></a>此内容包中包含的指标
“采购支出分析”内容包中包含一个由一组指标构成的报表。 这些指标显示为图表、磁贴和表。 下表概要介绍此内容包中的可视化。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>报表页</th>
<th>图表</th>
<th>磁贴</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>按供应商的采购</td>
<td><ul>
<li>按采购排名前 10 位的供应商（堆积条形图）</li>
<li>按供应商组/国家或地区/名称的采购总额（饼图）</li>
<li>按供应商组/国家或地区/名称的采购（柱形图）</li>
<li>按供应商组/国家或地区/名称的平均采购（柱形图）</li>
</ul></td>
<td><ul>
<li>采购总额</li>
<li>YOY 采购增长</li>
<li>供应商总数</li>
<li>有效供应商总数</li>
</ul></td>
</tr>
<tr class="even">
<td>按产品的采购</td>
<td><ul>
<li>按采购类别/产品名称的采购（柱形图）</li>
<li>按采购类别/产品名称的采购总额（饼图）</li>
<li>按采购排名前 10 位的产品（堆积条形图）</li>
</ul></td>
<td><ul>
<li>产品总数</li>
<li>产品总数中有效产品所占总百分比</li>
<li>占采购中的 80% 的产品的数量</li>
</ul></td>
</tr>
<tr class="odd">
<td>按期间的采购*</td>
<td><ul>
<li>按月/天的采购（柱形图）</li>
<li>累积采购 YOY 差异（瀑布图）</li>
<li>采购 YOY 增长总额（柱形图）</li>
<li>采购报表（矩阵）</li>
</ul></td>
<td><ul>
<li>YOY 采购增长</li>
<li>YOY 采购增长百分比</li>
</ul></td>
</tr>
<tr class="even">
<td>按供应商位置的采购</td>
<td><ul>
<li>按城市的采购</li>
<li>采购 YOY 增长百分比</li>
<li>按国家/地区的采购</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>按时间的采购支出分析</td>
<td><ul>
<li>按月/日的本年采购（折线图）</li>
<li>本年和去年的采购（折现柱形图）</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>按供应商的采购支出分析</td>
<td><ul>
<li>排名前 10 位的供应商所占采购百分比（漏斗图）</li>
<li>排名前 10 位的供应商（带 YOY 的增加支出）</li>
<li>排名前 10 位的供应商（带 YOY 的降低支出）</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* 今年和去年的采购，以及按采购类别的增长

## <a name="data-model-and-entities"></a>数据模型和实体
Dynamics 365 for Operations 数据用于“采购支出分析”内容包中的报表。 这些数据表示为实体商店（这是针对分析进行了优化的 Microsoft SQL 数据库）中暂存的聚合度量。 有关实体商店的详细信息，请参阅 [Power BI 与 Dynamics 中的实体商店之间的集成](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)博客文章。 此内容包中的聚合度量是 Microsoft Dynamics AX 2012 和 Microsoft Dynamics AX 2012 R3 中的采购多维数据集中提供的聚合度量子集。 若要在实体商店中暂存多维数据集的聚合度量，必须将其设置为可部署。 有关详细信息，请参阅 [Power BI 与 Dynamics 中的实体商店之间的集成](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)博客文章中在实体商店中暂存聚合度量的过程。 以下关键聚合度量直接从发票行实体提供，并用作此内容包的基础。

| 实体        | 关键聚合度量 | Dynamics 365 for Operations 的数据源 | 字段              | 说明                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| 发票行 | 采购                   | VendInvoiceTrans                            | SUM(LineAmountMST) | 以记帐币种计算的金额 |

下表显示内容包中通过发票行实体计算出的关键度量。

| 度量               | 计算                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| 本年的采购 | 本年的采购 = SUM('Invoice lines'\[Purchase\])                                            |
| 去年的采购    | 去年的采购 = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |
| YOY 采购增长   | YOY 采购增长 = \[Purchase current year\] – \[Purchase last year\]                            |

内容包中的以下关键维度用作筛选器以切分聚合度量，以便获得粒度更细微，更深入的分析洞察。

| 实体                 | 属性示例                                |
|------------------------|-------------------------------------------------------|
| 供应商                | 供应商组、供应商国家或地区、供应商名称 |
| 产品               | 产品编号、产品名称、物料组名称        |
| 采购类别 | 采购类别、采购类别名称      |
| 法人         | 法人姓名                                     |
| 日期                  | 日期、年偏移                                    |

默认情况下，此内容包显示当前日历年的数据。 但是，您可以更改报表筛选器部分中的数据筛选器。 还可以更改公司筛选器。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](..\data-entities\data-entities.md)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](configure-power-bi-integration.md)





