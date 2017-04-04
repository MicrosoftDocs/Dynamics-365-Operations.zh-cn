---
title: "销售和现金流入能力性能 Power BI 的内容"
description: "此主题描述在工序的 Dynamics 365 包括-销售和现金流入能力性能 Power BI 的内容包 Microsoft。 该说明如何访问用于创建内容包在内容包包括的语句并提供有关数据模型和实体的信息。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>销售和现金流入能力性能 Power BI 的内容

此主题描述在工序的 Dynamics 365 包括-销售和现金流入能力性能 Power BI 的内容包 Microsoft。 该说明如何访问用于创建内容包在内容包包括的语句并提供有关数据模型和实体的信息。

<a name="overview"></a>概览
--------

此内容包创建。销售经理可以监控、成本、收入和利润率销售关键度量。 为某工序使用从 Dynamics 365 的增值交易记录数据，并为客户和产品提供一公司范围销售数据的合计视图和销售业绩细分。 通过查看突出占收入更改并随着时间的推移，利润增长，报表可用于告知有关正值和负值趋势的经理和各个客户的产品。 类别和地区经理将查找很有用具有彼此比较不同的产品组和收入类别和客户现金流入能力领料迟钝的人员和引导符的图表。 绘制各个客户的收入和利润率的全面报表帐户提供管理员一个支持数据的基础调和他们的市场营销和增值到每个客户的各个模板。 销售和现金流入能力性能内容包将销售经理分析销售业绩：

-   收入，年初至今 (按客户组和各个客户、销售类别和单独的产品和地理)
-   收入连续多年，更改 (按客户) 销售地区和类别

可以分析现金流入量功能：

-   成本、毛利 (按客户组和增值产品类别)
-   成本变化，连续多年
-   客户现金流入能力 (按收入和毛利)

## <a name="accessing-the-content-pack"></a>访问内容包
销售和现金流入能力性能 Power BI 内容包在 Reporting Services Lifecycle Services (LCS) 过帐为实施资产，可以从 Dynamics (LCS) 工序的访问。 有关如何访问和启动 Power BI 报表的详细信息，请参阅在 [LCS 的 Power BI 的内容是从 Microsoft 和您的合作伙伴] (Microsoft partners.md BI 的内容。)

## <a name="metrics-included-in-the-content-pack"></a>度量中包含的内容包
内容包包括关联的图表平铺、直观的一组表和度量。的报表。 下表显示在内容包的直观的概览。

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **报表页面**        | **Charts**                                 | **平铺**                                               |
| 按客户的收入    | 按收入前 10 位的客户                | 总收入                                           |
|                        | 按客户组的总收入。            | YOY 收入增长                                      |
|                        | 按客户的平均用户和组 | 毛利                                            |
|                        | 收入和利润、按客户组   |                                                         |
| 收入副产品     | 按增值、成本和收入类别   | 总 \# 产品                                    |
|                        | 按收入的前 10 位产品                 | 可用产品的合计总数和百分比 |
|                        | 总收入按增值类别            | 占收入的产品编号 80%           |
| 按期间\*收入    | 按月份前收入                           | YOY 收入增长                                      |
|                        | 结尾的差异，YOY 收入             | YOY 收入增长。                                    |
|                        | 按客户区域的增值差异    |                                                         |
| 按位置的收入    | 按城市的销售收入                      |                                                         |
|                        | YOY 收入增长。                       |                                                         |
|                        | 乘以销售地域收入                    |                                                         |
| 客户现金流入量的能力。 | 毛利和收入，按客户   | 成本，则"毛利，YOY 收入增长          |
| 收益率分析 | 收入和利润、按月份之前          |                                                         |
|                        | 按毛利前 15 位的客户           |                                                         |
|                        | 按月份、成本，YOY 之前                 |                                                         |

此\* 收入和命名学习和发展按增值类别。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
工序数据的 Dynamics 365:用于填充时，会在销售和现金流入能力性能内容包的报表。 这表示为实体商店阶段，是为逻辑分析方法优化的 Microsoft SQL 数据库的聚合量化指标。 读取详细{{对：about}}此博客在 [与实体商店的 Power BI 集成的 Dynamics] (https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)。 {{在此：in}}内容包的聚合度量是可用在 Dynamics AX 2012 以及 AX 2012 R3 的多维数据集度量销售合计的子集。 若要阶段多维数据集的度量中聚合实体商店必须使它们可以部署。 有关详细信息，请参阅过程的阶段如何聚合到度量博客的 [与实体商店的 Power BI 集成实体商店的 Dynamics] (https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)。 使用发票行实体的以下参数聚合度量，内容包的基础。

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | **聚合关键度量**               | **的 Dynamics 365 **的工序数据源 | **Field**                                    | **Description**                          |
| 发票行 | 收入                                      | CustInvoiceTrans                                | 总计 (LineAmountMST)                           | 按记帐币种计算的金额            |
|               | 所售货物成本                           | InventTrans                                     | 总计 (CostAmountPosted + CostAmountAdjustment) | 成本额 + 调整                 |
|               | 佣金行金额–记帐币种 | CustInvoiceTrans                                | 总计 (CommissAmountMST)                        | 佣金记帐币种金额。 |

下表显示用于创建在内容包的数据集的若干发票行计算度量值聚合实体的关键度量。

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | ** **计算                                                                                |
| 毛利润      | 总计 (收入– COGS –在"客户发票行金额 (包括税) 的佣金销售代表)          |
| 毛利      | 总计 (、成本/收入- (在客户的发票行金额 (包括增值税)))             |
| 命名收入 | 命名收入= (发票计算总计 (“lines'entity_PLACEHOLDER \ [收入\])，SAMEPERIODLASTYEAR (日期\[日期\]) |

在的以下关键维度**销售**多维数据集作为切聚合度量的筛选器实现更佳的精细程度和更深入的见解分析。

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | ** **的属性示例                           |
| 客户        | 客户组，客户区域，地址，行业 |
| 产品         | 产品编号，产品名称，物料组名称       |
| 销售类别 | 增值类别名称                                 |
| 法人   | 法人名称                                   |
| 日期            | 日期                                                |

默认情况下，显示内容包数据当前日历年度，不过，您才能打开报表部分更改日期筛选器和筛选器。 您还可以更改公司筛选器。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](..\data-entities\data-entities.md)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](configure-power-bi-integration.md)



