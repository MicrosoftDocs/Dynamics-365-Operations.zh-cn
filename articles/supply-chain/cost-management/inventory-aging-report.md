---
title: 库龄报表示例和逻辑
description: 本主题提供了一些示例来展示如何解释库龄报表的结果。
author: RichardLuan
manager: AnnBe
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c165599c11b84e4064a9303d8b1f59558fc6b9d
ms.sourcegitcommit: 6bf8602333191e5161ba3a9ceecf160c85ff7e79
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484522"
---
# <a name="inventory-aging-report-examples-and-logic"></a>库龄报表示例和逻辑

[!include [banner](../includes/banner.md)]

本主题提供了一些示例来展示如何解释**库龄**报表的结果。 此报表将所选物料或物料组的现有数量和现有库存量值分类为几个期间段。 本主题还展示了报表的内部逻辑。

本主题中的示例展示了标准**库龄**报表中呈现的结果。 但是，通常，建议您使用此报表的[库龄报表存储](inventory-aging-report-storage.md)版本，尤其是当您有许多必须处理的物料和仓库时。 库龄报表存储保存您生成的每个报表，将结果显示为交互式页面和图表，并允许您导出任何已保存的报表。

## <a name="sample-data-that-is-used-in-these-examples"></a>这些示例中使用的示例数据

本主题中的示例基于本节中介绍的示例库存交易数据。

### <a name="storage-dimension-setup"></a>存储维度设置

示例系统包含以下存储维度设置。

| 姓名      | 活动 | 实际库存 | 财务库存 |
|-----------|--------|--------------------|---------------------|
| 站点      | 是    | 是                | 是                 |
| 存放地点 | 是    | 是                | 无                  |

### <a name="inventory-model"></a>库存模型

对于示例系统，已发布产品的库存模型为*先进先出*，此库存模型的**成本价**设置为*包括实际成本*。

### <a name="inventory-transactions"></a>库存交易记录

示例系统包含具有物料编号 *1000* 的已发布产品的以下库存交易记录。

| 参考      | 站点 | 存放地点 | 收货   | 发货 | 实际日期 | 财务日期 | 数量 | 成本金额 | 实际成本额 |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| 采购订单 | 1    | 11        | 已采购 |       | 3 月 15 日      | 3 月 15 日       | 10       | 1,000       | 1,000                |
| 采购订单 | 2    | 21        | 已采购 |       | 3 月 15 日      | 3 月 15 日       | 10       | 2,000       | 2,000                |
| 采购订单 | 1    | 11        | 已收到  |       | 4 月 15 日      |                | 5        |             | 375                  |
| 转移单 | 1    | 11        |           | 已售出  | 5 月 2 日         | 5 月 2 日          | -5       | -458.33     | -458.33              |
| 转移单 | 1    | 12        | 已采购 |       | 5 月 2 日         | 5 月 2 日          | 5        | 458.33      | 458.33               |
| 销售订单    | 1    | 12        |           | 已售出  | 5 月 3 日         | 5 月 3 日          | -1       | -91.67      | -91.67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>如何计算每个期间段内的数量和金额

通过使用前面几节中介绍的示例数据，您可以运行具有以下设置的**库龄**报表：

- **截止日期**：*2020 年 5 月 9 日*
- **站点**：*视图*
- **仓库**：*否*
- **物料编号**：*总计*
- **帐龄期间：** 将此字段设置为生成每月时段。

在此例中，生成的报表的内容类似于以下示例。

<table>
<thead>
<tr>
    <th rowspan="2">物料编号</th>
    <th rowspan="2">站点</th>
    <th rowspan="2">现有数量</th>
    <th rowspan="2">现有量值</th>
    <th rowspan="2">库存成本数量</th>
    <th rowspan="2">库存成本</th>
    <th rowspan="2">平均单位成本</th>
    <th colspan="2">2020 年 5 月 8 日 - 2020 年 5 月 1 日</th>
    <th colspan="2">2020 年 4 月 30 日 - 2020 年 4 月 1 日</th>
    <th colspan="2">2020 年 3 月 31 日 - 2020 年 3 月 1 日</th>
</tr>
<tr>
    <th>P1：数量</th>
    <th>P1：金额</th>
    <th>P2：数量</th>
    <th>P2：金额</th>
    <th>P3：数量</th>
    <th>P3：金额</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>9.00</td>
    <td>825.00</td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>总计 1000</strong></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2,825.00</strong></td>
</tr>
</tfoot>
</table>

请注意此示例报表中的以下详细信息：

- 报表中显示的**库存值数量**、**库存值**和**平均单位成本**值是财务库存维度的值（在此例中为**站点**）。

    例如，对于站点 1，报表显示以下信息：

    - **库存值数量**值是 *14* (= 10 + 5 – 5 + 5 – 1)。
    - **库存值**值是 *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67)。
    - **平均单位成本**值是 *91.67*。
    - 每个期间段中的**现有量值**值和**金额**值使用**平均单位成本**值计算得出。

- 此报表通过对每个期间段的总接收库存数量求和来确定每个期间段的现有数量。 然后，采用先进先出 (FIFO) 原则扣除总发货数量，不管物料使用的库存模型如何。

如果再次运行相同的报表，但是这次您将**站点**和**仓库**字段都设置为*视图*，新报表将类似于以下示例。

<table>
<thead>
<tr>
    <th rowspan="2">物料编号</th>
    <th rowspan="2">站点</th>
    <th rowspan="2">存放地点</th>
    <th rowspan="2">现有数量</th>
    <th rowspan="2">现有量值</th>
    <th rowspan="2">库存成本数量</th>
    <th rowspan="2">库存成本</th>
    <th rowspan="2">平均单位成本</th>
    <th colspan="2">2020 年 5 月 8 日 - 2020 年 5 月 1 日</th>
    <th colspan="2">2020 年 4 月 30 日 - 2020 年 4 月 1 日</th>
    <th colspan="2">2020 年 3 月 31 日 - 2020 年 3 月 1 日</th>
</tr>
<tr>
    <th>P1：数量</th>
    <th>P1：金额</th>
    <th>P2：数量</th>
    <th>P2：金额</th>
    <th>P3：数量</th>
    <th>P3：金额</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>916.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>5.00</td>
    <td>458.33</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>366.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td>4.00</td>
    <td>366.67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>总计 1000</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>366.67</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,458.33</strong></td>
</tr>
</tfoot>
</table>

这次，站点 1 分为两行，一行就仓库 11，另一行是仓库 12。 但是，**库存值数量**、**库存值**和**平均单位成本**值相同，因为**仓库**不是财务库存维度。

此外，请注意，站点 1 的数量分配不同。 在您运行的第一份报表中，系统忽略了同一站点中发生的转移单，从站点 1 的 **2020 年 3 月 31 日 - 2020 年 3 月 1 日**期间段中扣除了销售发票的数量。 但是，在新报表中，系统从仓库 12 的 **2020 年 5 月 8 日 - 2020 年 5 月 1 日**期间段中扣除了销售发票的数量。

## <a name="effects-of-inventory-closing"></a>库存结转的影响

如果您运行 5 月的库存结转，然后再次运行上一个报表，但是将**截止日期**字段设置为 *2020 年 5 月 31 日*，您将注意到以下结果：

- **库存值**和**平均单位成本**值已更新。
- 每个期间段的**现有量值**值和所有**金额**值已相应更新。

新报表将类似于以下示例。

<table>
<thead>
<tr>
    <th rowspan="2">物料编号</th>
    <th rowspan="2">站点</th>
    <th rowspan="2">存放地点</th>
    <th rowspan="2">现有数量</th>
    <th rowspan="2">现有量值</th>
    <th rowspan="2">库存成本数量</th>
    <th rowspan="2">库存成本</th>
    <th rowspan="2">平均单位成本</th>
    <th colspan="2">2020 年 5 月 31 日 - 2020 年 5 月 1 日</th>
    <th colspan="2">2020 年 4 月 30 日 - 2020 年 4 月 1 日</th>
    <th colspan="2">2020 年 3 月 31 日 - 2020 年 3 月 1 日</th>
</tr>
<tr>
    <th>P1：数量</th>
    <th>P1：金额</th>
    <th>P2：数量</th>
    <th>P2：金额</th>
    <th>P3：数量</th>
    <th>P3：金额</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>910.70</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>0.00</td>
    <td></td>
    <td>5.00</td>
    <td>455.36</td>
    <td>5.00</td>
    <td>455.36</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>364.29</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>4.00</td>
    <td>364.29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>总计 1000</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,275.00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>364.29</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>455.36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,455.36</strong></td>
</tr>
</tfoot>
</table>
