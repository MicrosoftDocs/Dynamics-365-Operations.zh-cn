---
title: 销售和收益率绩效 Power BI 内容
description: 此主题介绍销售和收益率绩效 Power BI 内容中的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。
author: ShylaThompson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SalesProfitabilityPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e74edfc5cf17499c080e825cf4b1fd39b6063e35
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182753"
---
# <a name="sales-and-profitability-performance-power-bi-content"></a>销售和收益率绩效 Power BI 内容

[!include [banner](../includes/banner.md)]

此主题介绍**销售和收益率绩效** Microsoft Power BI 内容中的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="overview"></a>概览

创建**销售和收益率绩效** Power BI 内容是为了让销售经理可以收入、毛利和利润率的关键销售指标。 它使用销售交易数据，并且同时提供公司范围的销售数据聚合视图和客户与产品的销售绩效分解。

报表突出显示收入和利润增长在一段时间内的变化。 因此，报表可用于提醒经理有关单个客户和产品的正负趋势的信息。 此外，图表比较不同产品类别和客户组之间的收入和收益率。 因此，类别和区域经理可以发现落后者和领先者。 最后，一份综合报表绘制单个客户的收入与利润率。 因此，帐户经理有一个以数据为支撑的基础可用来根据每位客户的模板调整其销售和市场营销工作。

销售经理可通过**销售和收益率绩效**内容按以下方式分析销售绩效：

- 收入、本年迄今（按客户组和单个客户、销售类别以及单个产品和地理位置）
- 收入变化、本年迄今（按客户区域和销售类别）

收益率可通过以下方式进行分析：

- 毛利润和毛利（按客户组和产品销售类别）
- 毛利润变化、各年
- 客户利润率（按收入与毛利）

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容
**销售和收益率绩效** Power BI 内容显示在**销售和收益率绩效**页面（**销售和市场** \> **查询和报表** \> **销售绩效分析** \> **销售和收益率绩效**）。

## <a name="metricsthat-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的度量
**销售和收益率绩效** Power BI 内容包括含有一组指标的报表。 这些指标显示为图表、磁贴和表。 下表概要介绍此内容中的可视化项。

| 报表页            | 图表                                     | 磁贴                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| 按客户的收入    | 按收入排名前 10 位的客户                | 总收入                                           |
|                        | 按客户组的总收入            | YOY 收入增长                                      |
|                        | 按客户组的平均客户收入 | 毛利                                            |
|                        | 按客户组的收入和毛利润   |                                                         |
| 按产品的收入     | 按销售类别的收入和毛利润   | 产品\#总数                                    |
|                        | 按收入排名前 10 位的产品                 | 有效产品总数和在总数中所占百分比 |
|                        | 按收入类别的总收入            | 占利润中的 80% 的产品的数量           |
| 按期间的收入\*    | 按月的收入                           | YOY 收入增长                                      |
|                        | 跟踪收入差异、YOY             | YOY 收入增长百分比                                    |
|                        | 按客户区域的销售总差异    |                                                         |
| 按位置的收入    | 按城市的销售收入                      |                                                         |
|                        | YOY 收入增长百分比                       |                                                         |
|                        | 按区域的销售收入                    |                                                         |
| 客户收益率 | 毛利与收入，按客户   | 毛利，毛利润，YOY 收入增长          |
| 收益率分析 | 按月的收入和毛利润          |                                                         |
|                        | 按毛利排名前 15 位的客户           |                                                         |
|                        | 按月的毛利润、YOY                 |                                                         |

\* 按销售类别的今年和去年收入，以及增长。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
以下数据用于填充**销售和收益率绩效** Power BI 内容中的报表。 此数据表示为实体商店内已分组的聚合度量。 实体商店是针对分析进行优化的 Microsoft SQL Server 数据库。 有关详细信息，请参阅 [Power BI 与实体商店集成概览](power-bi-integration-entity-store.md)。

此内容包中的聚合度量是 Microsoft Dynamics AX 2012 和 Microsoft Dynamics AX 2012 R3 中的销售多维数据集中提供的聚合度量子集。 若要在实体商店中暂存多维数据集的聚合度量，必须将其设置为可部署。 有关详细信息，请参阅 [Power BI 与 Dynamics 中的实体商店之间的集成](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)博客文章中在实体商店中暂存聚合度量的过程。

发票行实体的以下关键聚合度量用作此内容的基础。

| 实体        | 关键聚合度量                   | Dynamics 365 的数据源 | 字段                                        | 说明                                       |
|---------------|----------------------------------------------|------------------------------|----------------------------------------------|---------------------------------------------------|
| 发票行 | 收入                                      | CustInvoiceTrans             | SUM(LineAmountMST)                           | 以记帐币种计算的金额。            |
|               | 所售货物成本                           | InventTrans                  | SUM(CostAmountPosted + CostAmountAdjustment) | 成本额之和及调整。    |
|               | 佣金行金额 - 记帐币种 | CustInvoiceTrans             | SUM(CommissAmountMST)                        | 用记帐币种表示的佣金金额。 |

下表显示发票行实体的聚合度量，这些度量用于在内容的数据集中创建多个计算度量。

| 度量           | 计算                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| 毛利润      | SUM(Revenue – COGS – Commission – Sales tax (included in customer invoice line amount))          |
| 毛利      | SUM(Gross profit / (Revenue - Sales tax (included in customer invoice line amount)))             |
| 去年的收入 | 去年的收入 = CALCULATE(SUM('Invoice lines'\[Revenue\]), SAMEPERIODLASTYEAR(Dates\[Date\]) |

下表显示用作筛选器以切分聚合度量的销售多维数据集，以便获得粒度更细微，更深入的分析洞察。

| 实体           | 属性示例                               |
|------------------|------------------------------------------------------|
| 客户        | 客户组、客户区域、地址、行业 |
| 产品         | 产品编号、产品名称、物料组名称       |
| 销售类别 | 销售类别名称                                 |
| 法人   | 法人名称                                   |
| 日期            | 日期                                                |

默认情况下，此内容显示当前日历年的数据。 但是，您可以更改报表筛选器部分中的数据筛选器。 还可以更改公司筛选器。
