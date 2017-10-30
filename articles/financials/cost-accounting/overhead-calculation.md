---
title: "开销计算"
description: "此主题描述计算和分配间接成本的典型流程。"
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0ea6f7428cd5c7618d2d69f1fb66fd9539ad1073
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="overhead-calculation"></a>开销计算

[!include[banner](../includes/banner.md)]


此主题描述计算和分配间接成本的典型流程。

<a name="term-definition"></a>术语定义
---------------

间接成本是为业务运营支出的成本，但是不能直接归为任何具体的业务活动、产品或服务。 间接成本为营利活动的生成提供重要支持。 以下是一些开销成本示例：

-   租金
-   电
-   管理薪金

## <a name="overhead-calculation-overview"></a>开销计算概览
开销计算按正确顺序运行会计政策。 如果成本核算政策更改或检测到特定错误，您可以为同一个会计期间多次运行开销计算。 每次运行的开销计算将被存储并收到唯一版本 ID，让您可以比较各个版本的计算。 开销计算生成的成本条目接收会计日期。 此会计日期与计算中使用的会计期间的结束日期一致。 唯一版本 ID 由以下元素组成：

-   版本类型
-   日期和时间
-   成本核算分类帐
-   会计年度
-   会计期间

开销计算独立于版本运行。 因此，可以在实际版本前计算预算版本。 开销计算包括四个步骤，如下图所示。 在每个步骤中，创建包含日记帐条目的日记帐标头。 此日记帐标头为每个计算步骤保留输入数据。 政策和规则应用于每个日记帐行，成本条目生成为输出。 因此，您始终具有完全的可跟踪性。 

[![开销计算](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>计算和分摊电间接成本
在财务会计中，有些成本（如电）登记为总计。 因此，不为成本核算提供详细的管理洞察。 在成本核算中，为提供跨所有组织单位和级别的正确的管理洞察，成本必须流过各个组织单位。 此流必须基于消耗量的准确记录或公平评估。 在总帐中，可以过帐电成本，如下表所示。

<table>
<thead>
<tr>
<th>会计日期</th>
<th colspan="2">成本中心</th>
<th colspan="2">主科目</th>
<th>按记帐币种计算的金额</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 年 1 月 3 日</td>
<td>CC099</td>
<td>默认成本中心</td>
<td>10001</td>
<td>电</td>
<td>10,000.00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>步骤 1：处理成本行为计算

默认情况下，当成本条目从源数据导入时，它们在成本核算中接收**未分类**成本行为分类。 通过应用成本行为政策规则，您可以将成本条目重新分类为**固定成本**或**可变成本**。

#### <a name="define-the-cost-behavior-rule"></a>定义成本行为规则

在某些情况下，一部分成本是一项固定费用，其余成本基于消耗量。 通常电费帐单与此定义一致。 在支付特定固定费用后，您按千瓦时 (Kwh) 支付消耗量。 例如，如果固定成本费用为 1,000.00，以下是成本行为规则的定义：

-   固定金额 1,000.00
    -   0 &lt;= 1,000.00 = 固定
    -   1000,01 &lt; N = 可变

##### <a name="journal"></a>生产订单日记帐

<table>
<thead>
<tr>
<th>生产订单日记帐</th>
<th>日记帐类型</th>
<th colspan="3">会计日历期间</th>
<th>版本</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>成本行为计算日记帐</td>
<td>会计</td>
<td>2017</td>
<td>期间 1</td>
<td>开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>日记帐条目（成本对象余额日记帐条目）

<table>
<thead>
<tr>
<th>会计日期</th>
<th colspan="2">成本对象</th>
<th colspan="2">成本元素</th>
<th>成本行为</th>
<th>本币金额</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 年 1 月 3 日</td>
<td>CC099</td>
<td>默认成本中心</td>
<td>10001</td>
<td>电</td>
<td>未分类</td>
<td>10,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>成本条目

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th colspan="2">成本元素</th>
<th>成本行为</th>
<th>本币金额</th>
<th>会计日期</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>默认成本中心</td>
<td>10001</td>
<td>电</td>
<td>未分类</td>
<td>10,000.00</td>
<td>2017 年 1 月 3 日</td>
</tr>
<tr>
<td>CC099</td>
<td>默认成本中心</td>
<td>10001</td>
<td>电</td>
<td>未分类</td>
<td>-10,000.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC099</td>
<td>默认成本中心</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>1,000.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC099</td>
<td>默认成本中心</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>9,000.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
</tbody>
</table>

有关成本行为的详细信息，请参阅“成本行为政策”。 （请注意，此主题尚未完成，不过将很快推出。）

### <a name="step-2-process-the-cost-distribution-calculation"></a>步骤 2：处理成本分配计算

成本分配用于通过应用相关的分摊基数将成本从一个成本对象重新分配到一个或多个其他成本对象。 成本分配和成本分摊的不同之处在于，成本分配始终发生在原始成本的主要成本元素级别。

#### <a name="define-the-cost-distribution-rule"></a>定义成本分配规则

在财务会计中，电成本通常登记为总计。 在成本核算中，此方法不足够详细。 可变成本应公平分配到各个成本对象。 最合理的分配基础是电的消耗量 (Kwh)。 创建名为“电”的统计维度成员并记录电的消耗量。 默认情况下，所有统计维度成员均可作为分配基础。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>Kwh</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>1,000</td>
</tr>
<tr>
<td>CC002</td>
<td>财务</td>
<td>6,000</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>0</td>
</tr>
</tbody>
</table>

下表显示当电消耗量用作可变成本的分配基础时的结果。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>度量值</th>
<th>分配系数</th>
<th>本币金额</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>1,000</td>
<td>(1,000 ÷ 7,000) × 9,000.00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>财务</td>
<td>6,000</td>
<td>(6,000 ÷ 7,000) × 9,000.00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>0</td>
<td>(0 ÷ 7,000) × 9,000.00</td>
<td>0.00</td>
</tr>
</tbody>
</table>

固定成本应平均分配到消耗了电的单个成本对象。 可以通过在公式分配基础中使用电统计维度成员取得此结果：（电 &gt; 0.00）下表显示当电消耗量用作可变成本的分配基础时的结果。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>配方</th>
<th>度量值</th>
<th>分配系数</th>
<th>本币金额</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>(1,000 &gt; 0.00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1,000.00</td>
<td>500.00</td>
</tr>
<tr>
<td>CC002</td>
<td>财务</td>
<td>(6,000 &gt; 0.00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1,000.00</td>
<td>500.00</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>(0 &gt; 0.00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1,000.00</td>
<td>0.00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>生产订单日记帐

<table>
<thead>
<tr>
<th>生产订单日记帐</th>
<th>日记帐类型</th>
<th colspan="3">会计日历期间</th>
<th>版本</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>成本分配计算日记帐</td>
<td>会计</td>
<td>2017</td>
<td>期间 1</td>
<td>开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>日记帐条目（成本对象余额日记帐条目）

<table>
<thead>
<tr>
<th>会计日期</th>
<th colspan="2">成本对象</th>
<th colspan="2">成本元素</th>
<th>成本行为</th>
<th>本币金额</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC099</td>
<td>默认成本中心</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>1,000.00</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC099</td>
<td>默认成本中心</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>9,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>成本条目

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th colspan="2">成本元素</th>
<th>成本行为</th>
<th>本币金额</th>
<th>会计日期</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>默认成本中心</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>-1,000.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>500.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC002</td>
<td>财务</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>500.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC099</td>
<td>默认成本中心</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>-9,000.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>1,285.71</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC002</td>
<td>财务</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>7,714.29</td>
<td>2017 年 1 月 31 日</td>
</tr>
</tbody>
</table>

有关成本分配和分配基础的详细信息，请参阅“成本分配成本”和“分配基础”。 （请注意，此主题尚未完成，不过将很快推出。）

### <a name="step-3-process-the-overhead-rate-calculation"></a>步骤 3：处理开销比率计算

开销比率用于向一个或多个特定成本对象收费。 费用基于预先确定的成本率和来自指定的分配基础的度量值。 

#### <a name="define-the-overhead-rate"></a>定义开销比率

成本对象 CC001 HR 生成一组内部项目。 创建名为“HR 项目”的统计维度成员来测量消耗度量值。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>工时</th>
</tr>
</thead>
<tbody>
<tr>
<td>项目 1</td>
<td>项目 1</td>
<td>3</td>
</tr>
<tr>
<td>项目 2</td>
<td>项目 2</td>
<td>1</td>
</tr>
</tbody>
</table>

成本项目份额预先确定的成本率已定义。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>成本元素</th>
<th>成本行为</th>
<th>单位</th>
<th>比率</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>可变成本</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

下表显示 HR 项目用作分配基础时的结果。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>度量值</th>
<th>成本元素</th>
<th>分配系数</th>
<th>本币金额</th>
</tr>
</thead>
<tbody>
<tr>
<td>项目 1</td>
<td>项目 1</td>
<td>3</td>
<td>10001</td>
<td>(3 ÷ 1) × 10.00</td>
<td>30.00</td>
</tr>
<tr>
<td>项目 2</td>
<td>项目 2</td>
<td>1</td>
<td>10001</td>
<td>(1 ÷ 1) × 10.00</td>
<td>10.00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>生产订单日记帐

<table>
<thead>
<tr>
<th>生产订单日记帐</th>
<th>日记帐类型</th>
<th colspan="3">会计日历期间</th>
<th>版本</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>开销比率计算日记帐</td>
<td>会计</td>
<td>2017</td>
<td>期间 1</td>
<td>开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>日记帐条目（开销比率计算的日记帐条目）

<table>
<thead>
<tr>
<th>会计日期</th>
<th colspan="2">成本对象</th>
<th>度量值</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 年 1 月 31 日</td>
<td>项目 1</td>
<td>内部项目 1</td>
<td>3.00</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>项目 2</td>
<td>内部项目 2</td>
<td>1.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>成本条目

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th colspan="2">成本元素</th>
<th>成本行为</th>
<th>本币金额</th>
<th>会计日期</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>HR</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>-30.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>项目 1</td>
<td>内部项目 1</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>30.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>-10.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>项目 2</td>
<td>内部项目 2</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>10.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
</tbody>
</table>

有关开销比率政策的详细信息，请参阅“开销比率政策”和“分配基础”。 （请注意，此主题尚未完成，不过将很快推出。）

### <a name="step-4-process-the-cost-allocation-calculation"></a>步骤 4：处理成本分摊计算

分摊用于通过应用分配基础将成本对象的余额分配给其他成本对象。 Finance and Operations 支持互惠分摊方法。 在互惠分摊方法中，辅助成本对象交换的互助服务被完全识别。 系统自动确定执行分摊的正确顺序。 成本对象的余额按单一分配基础分配。 支持跨成本对象维度及其各自成员的分摊。 分摊顺序由成本控制单元控制。 

[![互惠方法](./media/reciprocal-method.png)](./media/reciprocal-method.png)

#### <a name="define-the-cost-allocation"></a>定义成本分摊

这是说明如何跟踪成本流的简单示例。 成本对象 CC001 HR 生成若干成本对象。 创建名为“HR 服务”的统计维度成员来测量消耗度量值。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>HR 服务</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>财务</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>包装</td>
<td>10</td>
</tr>
</tbody>
</table>

成本对象 CC002 财务生成若干成本对象。 创建名为“财务服务”的统计维度成员来测量消耗度量值。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>财务服务</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>包装</td>
<td>35</td>
</tr>
</tbody>
</table>

成本对象 CC003 装配生成若干成本对象。 创建名为“装配服务”的统计维度成员来测量消耗度量值。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>装配服务（小时）</th>
</tr>
</thead>
<tbody>
<tr>
<td>产品 1</td>
<td>产品 1</td>
<td>60</td>
</tr>
<tr>
<td>产品 2</td>
<td>产品 2</td>
<td>20</td>
</tr>
</tbody>
</table>

成本对象 CC004 包装生成若干成本对象。 创建名为“包装服务”的统计维度成员来测量消耗度量值。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>包装服务（小时）</th>
</tr>
</thead>
<tbody>
<tr>
<td>产品 1</td>
<td>产品 1</td>
<td>80</td>
</tr>
<tr>
<td>产品 2</td>
<td>产品 2</td>
<td>15</td>
</tr>
</tbody>
</table>

**注意：**在 Finance and Operations 中，产品消耗的生产工时等统计度量可以派生自源数据。 关于统计度量的更多详细信息，请参阅“统计度量提供方模板”。 （请注意，此主题尚未完成，不过将很快推出。）下表显示 HR 服务用作总成本的分配基础时的结果（固定成本和可变成本）。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>度量值</th>
<th>分配系数</th>
<th>本币金额</th>
<th>成本行为</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>财务</td>
<td>35</td>
<td>(35 ÷ 100) × 500.00</td>
<td>175.00</td>
<td>固定成本</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>55</td>
<td>(55 ÷ 100) × 500.00</td>
<td>275.00</td>
<td>固定成本</td>
</tr>
<tr>
<td>CC004</td>
<td>包装</td>
<td>10</td>
<td>(10 ÷ 100) × 500.00</td>
<td>50.00</td>
<td>固定成本</td>
</tr>
<tr>
<td>CC002</td>
<td>财务</td>
<td>35</td>
<td>(35 ÷ 100) × 1,245.71</td>
<td>436.00</td>
<td>可变成本</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>55</td>
<td>(55 ÷ 100) × 1,245.71</td>
<td>685.14</td>
<td>可变成本</td>
</tr>
<tr>
<td>CC004</td>
<td>包装</td>
<td>10</td>
<td>(10 ÷ 100) × 1,245.71</td>
<td>124.57</td>
<td>可变成本</td>
</tr>
</tbody>
</table>

下表显示当财务服务用作总成本的分配基础时的结果（固定成本和可变成本）。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>度量值</th>
<th>分配系数</th>
<th>本币金额</th>
<th>成本行为</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>65</td>
<td>(65 ÷ 100) × (500.00 + 175.00)</td>
<td>438.75</td>
<td>固定成本</td>
</tr>
<tr>
<td>CC004</td>
<td>包装</td>
<td>35</td>
<td>(35 ÷ 100) × (500.00 + 175.00)</td>
<td>236.25</td>
<td>固定成本</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>65</td>
<td>(65 ÷ 100) × (7,714.29 + 436.00)</td>
<td>5,297.69</td>
<td>可变成本</td>
</tr>
<tr>
<td>CC004</td>
<td>包装</td>
<td>35</td>
<td>(35 ÷ 100) × (7,714.29 + 436.00)</td>
<td>2,852.60</td>
<td>可变成本</td>
</tr>
</tbody>
</table>

下表显示当装配服务用作总成本的分配基础时的结果（固定成本和可变成本）。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>度量值</th>
<th>分配系数</th>
<th>本币金额</th>
<th>成本行为</th>
</tr>
</thead>
<tbody>
<tr>
<td>产品 1</td>
<td>产品 1</td>
<td>60</td>
<td>(60 ÷ 80) × (275.00 + 438.75)</td>
<td>535.31</td>
<td>固定成本</td>
</tr>
<tr>
<td>产品 2</td>
<td>产品 2</td>
<td>20</td>
<td>(20 ÷ 80) × (275.00 + 438.75)</td>
<td>178.44</td>
<td>固定成本</td>
</tr>
<tr>
<td>产品 1</td>
<td>产品 1</td>
<td>60</td>
<td>(60 ÷ 80) × (5,297.69 + 685.14)</td>
<td>4,487.12</td>
<td>可变成本</td>
</tr>
<tr>
<td>产品 2</td>
<td>产品 2</td>
<td>20</td>
<td>(20 ÷ 80) × (5,297.69 + 685.14)</td>
<td>1,495.71</td>
<td>可变成本</td>
</tr>
</tbody>
</table>

下表显示当包装服务用作总成本的分配基础时的结果（固定成本和可变成本）。

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th>度量值</th>
<th>分配系数</th>
<th>本币金额</th>
<th>成本行为</th>
</tr>
</thead>
<tbody>
<tr>
<td>产品 1</td>
<td>产品 1</td>
<td>80</td>
<td>(80 ÷ 95) × (50.00 + 236.25)</td>
<td>241.05</td>
<td>固定成本</td>
</tr>
<tr>
<td>产品 2</td>
<td>产品 2</td>
<td>15</td>
<td>(15 ÷ 95) × (50.00 + 236.25)</td>
<td>45.20</td>
<td>固定成本</td>
</tr>
<tr>
<td>产品 1</td>
<td>产品 1</td>
<td>80</td>
<td>(80 ÷ 95) × (2,852.60 + 124.57)</td>
<td>2,507.09</td>
<td>可变成本</td>
</tr>
<tr>
<td>产品 2</td>
<td>产品 2</td>
<td>15</td>
<td>(15 ÷ 95) × (2,852.60 + 124.57)</td>
<td>470.08</td>
<td>可变成本</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>日记帐条目（成本对象余额日记帐条目）

<table>
<thead>
<tr>
<th>生产订单日记帐</th>
<th>日记帐类型</th>
<th colspan="3">会计日历期间</th>
<th>版本</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>成本分配日记帐</td>
<td>会计</td>
<td>2017</td>
<td>期间 1</td>
<td>开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>日记帐行

<table>
<thead>
<tr>
<th>会计日期</th>
<th colspan="2">成本对象</th>
<th colspan="2">成本元素</th>
<th>成本行为</th>
<th>本币金额</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>500.00</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>1,245.71</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC002</td>
<td>财务</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>675.00</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC002</td>
<td>财务</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>8,150.29</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC003</td>
<td>程序集</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>713.75</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC003</td>
<td>程序集</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>5,982.83</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC003</td>
<td>包装</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>286.25</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC003</td>
<td>包装</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>2,977.17</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>产品 1</td>
<td>产品 1</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>776.36</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>产品 1</td>
<td>产品 1</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>6,994.21</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>产品 2</td>
<td>产品 1</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>223.64</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>产品 2</td>
<td>产品 1</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>成本条目

<table>
<thead>
<tr>
<th colspan="2">成本对象</th>
<th colspan="2">成本元素</th>
<th>成本行为</th>
<th>本币金额</th>
<th>会计日期</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>-500.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC002</td>
<td>财务</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>175.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>275.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC004</td>
<td>包装</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>50,00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>-1,245.71</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC002</td>
<td>财务</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>436.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>685.14</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC004</td>
<td>包装</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>124.57</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC002</td>
<td>财务</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>-675.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>438.75</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC004</td>
<td>包装</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>236.25</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC002</td>
<td>财务</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>-8,150.29</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>5,297.69</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC004</td>
<td>包装</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>2,852.60</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>-713.75</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>产品 1</td>
<td>产品 1</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>535.31</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>产品 2</td>
<td>产品 2</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>178.44</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>-5,982.83</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>产品 1</td>
<td>产品 1</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>4,487.12</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>产品 2</td>
<td>产品 2</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>1,495.71</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>-286.25</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>产品 1</td>
<td>产品 1</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>241.05</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>产品 2</td>
<td>产品 2</td>
<td>10001</td>
<td>电</td>
<td>固定成本</td>
<td>45.20</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>程序集</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>-2,977.17</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>产品 1</td>
<td>产品 1</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>2,507.09</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>产品 2</td>
<td>产品 2</td>
<td>10001</td>
<td>电</td>
<td>可变成本</td>
<td>470.08</td>
<td>2017 年 1 月 31 日</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>结论
在财务会计中，10,000.00 电成本过帐到虚拟成本中心 ID。 因此，成本会计员将了解必须分摊此成本。 在成本核算中，跨组织单位和级别的成本流，基于所应用的政策和规则。 每项成本已与为成本分摊提供最佳评估的分配基础关联。

<table>
<thead>
<tr>
<th colspan="2" rowspan="2">成本元素</th>
<th colspan="9">成本对象</th>
<th rowspan="2">合计</th>
</tr>
<tr>
<th>CC099</th>
<th>CC001</th>
<th>CC002</th>
<th>CC003</th>
<th>CC004</th>
<th>项目 1</th>
<th>项目 2</th>
<th>产品 1</th>
<th>产品 2</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">10001 电</td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><strong>30.00</strong></td>
<td style="text-align: right;"><strong>10.00</strong></td>
<td style="text-align: right;"><strong>7,770.57</strong></td>
<td style="text-align: right;"><strong>2,189.43</strong></td>
<td style="text-align: right;"><strong>10,000.00</strong></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;">未分类</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">固定成本</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;">776.36</td>
<td style="text-align: right;">223.64</td>
<td style="text-align: right;"><strong>1,000.00</strong></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">可变成本</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;">0.00</td>
<td style="text-align: right;">30.00</td>
<td style="text-align: right;">10.00</td>
<td style="text-align: right;">6,994.21</td>
<td style="text-align: right;">1,965.79</td>
<td style="text-align: right;"><strong>9,000.00</strong></td>
</tr>
</tbody>
</table>

> [!NOTE]
> 此主题显示主要成本元素“10001 电”如何流过成本对象。 因此，此间接成本分摊到组织的最低级别。 换言之，最低级别的成本对象承担成本。 如果您需要成本对象之间的可视成本流，可以使用成本累积政策规则实现成本流可视化。 更多详细信息，请参阅“成本累积政策”。 （请注意，此主题尚未完成，不过将很快推出。）




