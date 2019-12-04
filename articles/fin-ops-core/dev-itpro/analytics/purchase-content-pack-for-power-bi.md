---
title: 采购花费分析 Power BI 内容
description: 此主题介绍采购支出分析 Power BI 内容中的内容。 它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2d31aaf14f6399baca8531707864c48cd2d56ac2
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769963"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>采购花费分析 Power BI 内容

[!include [banner](../includes/banner.md)]

此主题介绍**采购支出分析** Microsoft Power BI 内容中的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="overview"></a>概览

**采购支出分析** Power BI 内容的设计是为了帮助采购经理和负责预算的经理跟踪采购支出。 经理可以通过以下方式分析采购支出：

- 本年迄今的采购（按供应商组和单个供应商、采购类别和单个产品，以及供应商位置）
- 各年的采购变化（按供应商组和采购类别）

该内容使用采购交易数据，并且同时提供公司范围的采购数据聚合视图和按供应商与产品分类的采购支出分解。 报表突出显示一段时间的采购支出变化。 因此，这些报表可用于提醒经理有关单个供应商和产品的正负支出趋势的信息。 此外，图表显示不同采购类别和供应商组的采购支出。 因此，类别和区域经理可以使用这些图表来帮助识别支出行为的变化。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容
**采购花费分析** Power BI 内容显示在**采购和花费分析**页面（**采购** \> **查询和报表** \> **采购绩效分析** \> **采购和花费分析**）。

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的度量
**采购支出分析** Power BI 内容中包含一个由一组指标构成的报表。 这些指标显示为图表、磁贴和表。 

以下部分提供对可视化项的概览。

### <a name="purchase-by-vendor-report-page"></a>按供应商的采购报表页面
**图表**
- 按采购排名前 10 位的供应商（堆积条形图）
- 按供应商组/国家或地区/名称的采购总额（饼图）
- 按供应商组/国家或地区/名称的采购（柱形图）
- 按供应商组/国家或地区/名称的平均采购（柱形图）

**磁贴**
- 采购总额
- YOY 采购增长
- 供应商总数
- 有效供应商总数

**示例**
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>按产品的采购报表页面

**图表**
- 按采购类别/产品名称的采购（柱形图）
- 按采购类别/产品名称的采购总额（饼图）
- 按采购排名前 10 位的产品（堆积条形图）

**磁贴**
- 产品总数</li>
- 产品总数中有效产品所占总百分比
- 占采购中的 80% 的产品的数量

**示例**


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>按期间的采购报表页面
此页中显示 今年和去年的采购，以及按采购类别的采购。

**图表** 
- 按月/天的采购（柱形图）
- 累积采购 YOY 差异（瀑布图）
- 采购 YOY 增长总额（柱形图）
- 采购报表（矩阵）

**磁贴**
- YOY 采购增长
- YOY 采购增长百分比

**示例**
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>按供应商位置的采购报表页面

**图表**
- 按城市的采购
- 采购 YOY 增长百分比
- 按国家/地区的采购

**示例**
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>按时间的采购报表页面

**图表** 
- 按月/日的本年采购（折线图）
- 本年和去年的采购（折现柱形图）

**示例**
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>按供应商的采购报表页面

**图表** 
- 排名前 10 位的供应商所占采购百分比（漏斗图）
- 排名前 10 位的供应商（带 YOY 的增加支出）
- 排名前 10 位的供应商（带 YOY 的降低支出）

**示例** 
<img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>数据模型和实体
以下数据用于填充**采购支出分析** Power BI 内容中的报表页。 此数据表示为实体商店内已分组的聚合度量。 实体商店是针对分析进行优化的 Microsoft SQL Server 数据库。 有关详细信息，请参阅 [Power BI 与实体商店集成](power-bi-integration-entity-store.md)。

此内容包中的聚合度量是 Microsoft Dynamics AX 2012 和 Microsoft Dynamics AX 2012 R3 中的采购多维数据集中提供的聚合度量子集。 若要在实体商店中暂存多维数据集的聚合度量，必须将其设置为可部署。 有关详细信息，请参阅 [Power BI 与实体商店集成](power-bi-integration-entity-store.md)中在实体商店中暂存聚合度量的过程。 以下关键聚合度量直接从发票行实体提供，并用作此内容的基础。

| 实体        | 关键聚合度量 | 数据源                                 | 字段              | 说明                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| 发票行 | 采购                   | VendInvoiceTrans                            | SUM(LineAmountMST) | 以记帐币种计算的金额。 |

下表显示内容中通过发票行实体计算出的关键度量。

| 度量               | 计算                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| 本年的采购 | 本年的采购 = SUM('Invoice lines'\[Purchase\])                                            |
| 去年的采购    | 去年的采购 = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |
| YOY 采购增长   | YOY 采购增长 = \[Purchase current year\] – \[Purchase last year\]                            |

内容中的以下关键维度用作筛选器以切分聚合度量，以便获得粒度更细微，更深入的分析洞察。

| 实体                 | 属性示例                                |
|------------------------|-------------------------------------------------------|
| 供应商                | 供应商组、供应商国家或地区、供应商名称 |
| 产品               | 产品编号、产品名称、物料组名称        |
| 采购类别 | 采购类别、采购类别名称      |
| 法人         | 法人姓名                                     |
| 日期                  | 日期、年偏移                                    |

默认情况下，此内容显示当前日历年的数据。 但是，您可以更改报表筛选器部分中的数据筛选器。 还可以更改公司筛选器。
