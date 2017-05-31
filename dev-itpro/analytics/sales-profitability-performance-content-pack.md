---
title: "销售和收益率绩效 Power BI 内容"
description: "此主题介绍适用于 Microsoft Power BI 的 Dynamics 365 for Operations - 销售和收益率绩效内容包中的内容。 它说明如何访问内容包中包括的报表，并提供有关用于构建内容包的数据模型和实体的信息。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 357f7071d801b13518c83170f8d0e7946dd9dede
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>销售和收益率绩效 Power BI 内容

[!include[banner](../includes/banner.md)]


此主题介绍适用于 Microsoft Power BI 的 Dynamics 365 for Operations - 销售和收益率绩效内容包中的内容。 它说明如何访问内容包中包括的报表，并提供有关用于构建内容包的数据模型和实体的信息。

<a name="overview"></a>概览
--------

此内容包是为销售经理创建的，用于监控收入、毛利和利润率的关键销售指标。 它使用来自 Dynamics 365 for Operations 的销售交易数据，并且同时提供公司范围的销售数据聚合视图和客户与产品的销售绩效分解。 通过突出显示一段时间的收入和利润增长变化，可以将报表用于提醒经理有关单个客户和产品的正负趋势。 类别和区域经理将发现图表非常有用，可用于彼此比较不同产品类别和客户组的收入和收益率，以选出落后者和领先者。 绘制单个客户的收入与利润率的负荷报表可供帐户经理作为数据支持基础，以根据每位客户各自的配置文件调整客户的销售和市场营销工作。 销售经理可通过销售和收益率绩效内容包，按以下条件分析销售绩效：

-   收入、本年迄今（按客户组和单个客户、销售类别以及单个产品和地理位置）
-   收入变化、本年迄今（按客户区域和销售类别）

可以按以下条件分析收益率：

-   毛利润和毛利（按客户组和产品销售类别）
-   毛利润变化、各年
-   客户利润率（按收入与毛利）

## <a name="accessing-the-content-pack"></a>访问内容包
“销售和利润率绩效 Power BI ”内容包发布为 Lifecycle Services (LCS) 中的实施资产，并且可以从 Dynamics 365 for Operations 访问。 有关如何访问和启动 Power BI 报表的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。
**注意：**KB 4011327 是此 Power BI 内容的先决条件。 登录 Lifecycle Services 之后，可以在以下位置访问该 KB：<a href="https://fix.lcs.dynamics.com/issue/results/?q=kb4011327">https://fix.lcs.dynamics.com/issue/results/?q=kb4011327</a>。

## <a name="metrics-included-in-the-content-pack"></a>此内容包中包含的指标
此内容包中包含一个由一组显示为图表、磁贴和表的指标构成的报表。 下表概要介绍此内容包中的可视化。

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **报表页**        | **图表**                                 | **磁贴**                                               |
| 按客户的收入    | 按收入排名前 10 位的客户                | 总收入                                           |
|                        | 按客户组的总收入            | YOY 收入增长                                      |
|                        | 按客户组的平均客户收入 | 毛利                                            |
|                        | 按客户组的收入和毛利润   |                                                         |
| 按产品的收入     | 按销售类别的收入和毛利润   | 产品总数                                    |
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
Dynamics 365 for Operations 数据用于填充销售和收益率绩效内容包中的报表。 表示为实体商店（这是针对分析进行了优化的 Microsoft SQL 数据库）中暂存的聚合度量。 有关详细信息，请阅读博客 [Power BI 与 Dynamics 中的实体商店的集成](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)。 此内容包中的聚合度量是 Dynamics AX 2012 和 AX 2012 R3 中的销售多维数据集中提供的聚合度量子集。 若要在实体商店中暂存多维数据集的聚合度量，必须将其设置为可部署。 有关详细信息，请参阅 [Power BI 与 Dynamics 中的实体商店之间的集成](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)博客中如何将聚合度量暂存到实体商店中的过程。 发票行实体的以下关键聚合度量用作此内容包的基础。

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **实体**    | **关键聚合度量**               | **Dynamics 365 for Operations 的数据源** | **字段**                                    | **描述**                          |
| 发票行 | 收入                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | 按记帐币种计算的金额            |
|               | 所售货物成本                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | 成本额 + 调整                 |
|               | 佣金行金额 - 记帐币种 | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | 记帐币种的佣金金额 |

下表显示发票行实体的聚合度量，这些度量用于在内容包的数据集中创建多个计算度量。

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **度量**       | **计算方法**                                                                                |
| 毛利润      | SUM(Revenue – COGS – Commission – Sales tax (included in customer invoice line amount))          |
| 毛利      | SUM(Gross profit / (Revenue - Sales tax (included in customer invoice line amount)))             |
| 去年的收入 | 去年的收入 = CALCULATE(SUM('Invoice lines'\[Revenue\]), SAMEPERIODLASTYEAR(Dates\[Date\]) |

**销售多维数据集**中的以下关键维度用作筛选器以切分聚合度量，以便获得粒度更细微，更深入的分析洞察。

|                  |                                                      |
|------------------|------------------------------------------------------|
| **实体**       | **属性示例**                           |
| 客户        | 客户组、客户区域、地址、行业 |
| 产品         | 产品编号、产品名称、物料组名称       |
| 销售类别 | 销售类别名称                                 |
| 法人   | 法人名称                                   |
| 日期            | 日期                                                |

默认情况下，此内容包显示当前日历年度的数据，但是可以打开报表筛选器区域并更改数据筛选器。 还可以更改公司筛选器。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](..\data-entities\data-entities.md)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](configure-power-bi-integration.md)





