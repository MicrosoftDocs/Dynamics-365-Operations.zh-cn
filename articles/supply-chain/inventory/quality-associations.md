---
title: 质量关联
description: 本主题介绍如何使用 Microsoft Dynamics 365 Supply Chain Management 中的质量关联来自动生成与您的销售、采购和生产流程相关的质检订单。
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28984730e5660414eec1ba087eb5de1eba4cbbb8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571921"
---
# <a name="quality-associations"></a>质量关联

[!include [banner](../includes/banner.md)]

本主题介绍如何使用 Microsoft Dynamics 365 Supply Chain Management 中的质量关联来自动生成与您的销售、采购和生产流程相关的质检订单。

质量关联定义生成的质检订单的所有以下信息：

- 交易记录事件
- 必须在物料上执行的测试组
- 可接受质量级别 (AQL)
- 抽样计划

您必须为业务流程中要求自动生成质检订单的每种变化定义质量关联。 例如，可以在业务流程中为采购订单、检验单、销售订单和生产订单生成质检订单。

## <a name="working-with-quality-associations"></a>使用质量关联

使用质量关联的业务流程可与许多源文档相关，例如采购订单、销售订单或生产订单。

每个质量关联记录定义了测试组、AQL 和应用于生成的质检订单的抽样计划。 您必须为业务流程中每个变化形式定义质量关联记录。 例如，当更新采购订单产品收据时，您可以设置生成质检订单的质量关联。 根据执行计划的设置，在存在未结质检订单的情况下，可以锁定触发流程本身。 或者，可以锁定后续流程，如采购订单开票。

> [!NOTE]
> 在有未结质检订单时，会自动锁定库存数量使其不发放。 根据 **物料抽样** 页上的 **完全锁定** 字段的设置，该数量是质检订单上的数量或源文档行上的数量。 有关详细信息，请参阅[质量管理物料抽样](quality-item-sampling.md)。

对于给定业务流程，质量关联记录标识用于生成质检订单的事件和条件。 条件可以特定于站点或法人。 只有对于事件存在现有库存时，才能生成涉及破坏性测试的质检订单。

要使用质量关联，转到 **库存管理 \> 设置 \> 质量控制 \> 质量关联**。 以下示例演示如何为各个业务流程中的变化形式定义质量关联记录。 对于每个示例，下表总结了质量关联记录定义的事件和条件。

<table>
<thead>
<tr>
<th>引用类型</th>
<th>事件类型</th>
<th>执行</th>
<th>事件锁定</th>
<th>文档引用</th>
</tr>
</thead>
<tbody>
<tr>
<td>库存</td>
<td>不适用</td>
<td>不适用</td>
<td>无</td>
<td>全部</td>
</tr>
<tr>
<td rowspan="7">销售额</td>
<td rowspan="4">已计划领料流程</td>
<td rowspan="4">之前</td>
<td>无</td>
<td rowspan="22">仅特定 ID、组或全部</td>
</tr>
<tr>
<td>领料流程</td>
</tr>
<tr>
<td>装箱单</td>
</tr>
<tr>
<td>开票</td>
</tr>
<tr>
<td rowspan="3">装箱单</td>
<td rowspan="3">之前</td>
<td>无</td>
</tr>
<tr>
<td>装箱单</td>
</tr>
<tr>
<td>开票</td>
</tr>
<tr>
<td rowspan="15">采购</td>
<td rowspan="7">收货清单</td>
<td rowspan="4">之前</td>
<td>无</td>
</tr>
<tr>
<td>收货清单</td>
</tr>
<tr>
<td>物料收货</td>
</tr>
<tr>
<td>开票</td>
</tr>
<tr>
<td rowspan="3">之后</td>
<td>无</td>
</tr>
<tr>
<td>物料收货</td>
</tr>
<tr>
<td>开票</td>
</tr>
<tr>
<td rowspan="3">注册</td>
<td rowspan="3">不适用</td>
<td>无</td>
</tr>
<tr>
<td>物料收货</td>
</tr>
<tr>
<td>开票</td>
</tr>
<tr>
<td rowspan="5">物料收货</td>
<td rowspan="3">之前</td>
<td>无</td>
</tr>
<tr>
<td>物料收货</td>
</tr>
<tr>
<td>开票</td>
</tr>
<tr>
<td rowspan="2">之后</td>
<td>无</td>
</tr>
<tr>
<td>开票</td>
</tr>
<tr>
<td rowspan="8">生产</td>
<td rowspan="3">注册</td>
<td rowspan="3">不适用</td>
<td>无</td>
<td rowspan="12">全部</td>
</tr>
<tr>
<td>完工入库</td>
</tr>
<tr>
<td>结束</td>
</tr>
<tr>
<td rowspan="5">完工入库</td>
<td rowspan="3">之前</td>
<td>无</td>
</tr>
<tr>
<td>完工入库</td>
</tr>
<tr>
<td>结束</td>
</tr>
<tr>
<td rowspan="2">之后</td>
<td>无</td>
</tr>
<tr>
<td>结束</td>
</tr>
<tr>
<td rowspan="4">检验</td>
<td rowspan="3">完工入库</td>
<td rowspan="2">之前</td>
<td>完工入库</td>
</tr>
<tr>
<td>结束</td>
</tr>
<tr>
<td>之后</td>
<td>结束</td>
</tr>
<tr>
<td>结束</td>
<td>之前</td>
<td>结束</td>
</tr>
<tr>
<td rowspan="3">工艺路线工序</td>
<td rowspan="3">报告为完工入库</td>
<td rowspan="2">之前</td>
<td>无</td>
<td rowspan="3">特定 ID、组或全部，以及特定资源、组或全部</td>
</tr>
<tr>
<td>报告为完工入库</td>
</tr>
<tr>
<td>之后</td>
<td>无</td>
</tr>
<tr>
<td rowspan="3">联产品生产</td>
<td>注册</td>
<td>不适用</td>
<td rowspan="3">无</td>
<td rowspan="3">所有</td>
</tr>
<tr>
<td rowspan="2">报告为完工入库</td>
<td>之前</td>
</tr>
<tr>
<td>之后</td>
</tr>
</tbody>
</table>

> [!NOTE]
> *仓库流程质量管理* 功能添加了将 **事件类型** 字段设置为 *报告为完工入库* 并将 **执行** 字段设置为 *以后* 的生产的质检订单处理能力，以及将 **事件类型** 字段设置为 *登记* 的采购的质检订单处理能力。 有关详细信息，请参阅[仓库流程质量管理](quality-management-for-warehouses-processes.md)。

下表提供有关可以如何为特定类型的流程生成质检订单的详细信息。

<div class="tableSection">
<table>
<thead>
<tr>
<th>流程的类型</th>
<th>可以自动生成质检订单时</th>
<th>需要破坏性测试的情况下可以生成质检订单时</th>
<th>条件信息</th>
<th>手动生成信息</th>
</tr>
</thead>
<tbody>
<tr>
<td>采购订单</td>
<td>过帐收到的物料的收据清单或产品收据之前或之后</td>
<td>过帐收到的物料的产品收据之后，因为物料必须可用于破坏性测试</td>
<td>质检订单的要求可以反映特定的站点、物料或供应商，或者反映这些条件的组合。</td>
<td>引用某一采购订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</td>
</tr>
<tr>
<td>检验单</td>
<td>在检验单报告为已完工入库或已结束之前或之后</td>
<td>无法生成需要破坏性测试的质检订单。 假定检验单功能处理损坏物料的处置。</td>
<td>质检订单的要求可以反映特定的站点、物料或供应商，或者反映这些条件的组合。</td>
<td>引用某一检验单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</td>
</tr>
<tr>
<td>销售订单</td>
<td>在要被装运的物料的已计划领料流程或装箱单更新之前</td>
<td>任何步骤中</td>
<td>质检订单的要求可以反映特定的站点、物料或客户，或者反映这些条件的组合。</td>
<td>引用某一销售订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</td>
</tr>
<tr>
<td>生产订单</td>
<td>报告生产订单的完工数量之前或之后</td>
<td>报告生产订单的完工数量之后</td>
<td>质检订单的要求可以反映特定站点或物料，或者反映这些条件的组合。</td>
<td>引用某一生产订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</td>
</tr>
<tr>
<td>具有工艺路线工序的生产订单</td>
<td>在报告为已完成工序之前或之后</td>
<td>在报告生产最后一道工序完成后</td>
<td>质检订单的要求可以反映特定的站点、物料或运营资源，或者反映这些条件的组合。</td>
<td>引用某一工艺路线工序的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</td>
</tr>
<tr>
<td>库存</td>
<td>无法为库存日志中的交易记录或为转移单交易记录自动生成质检订单。</td>
<td></td>
<td></td>
<td>必须为物料的库存数量手动创建质检订单。 实际现有库存量是必需的。</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>自动生成质检订单示例

### <a name="purchasing"></a>采购

在采购中，如果您在 **质量关联** 页面上将 **事件类型** 字段设置为 *物料收货*，并将 **执行** 字段设置为 *之后*，您将得到以下结果：

- 如果将 **按照更新的数量** 选项设置为 *是*，则会根据物料抽样中收到的数量和设置，根据采购订单为每个收货生成质检订单。 每次根据采购订单接收数量时，都会根据新接收的数量生成新的质检订单。
- 如果将 **按照更新的数量** 选项设置为 *否*，则会根据收到的数量，根据采购订单为第一个收货生成质检订单。 此外，根据跟踪维度，将基于剩余数量创建一个或多个质检订单。 不会根据采购订单为后续收货生成质检订单。

### <a name="production"></a>生产

在生产中，如果您在 **质量关联** 页面上将 **事件类型** 字段设置为 *完工入库*，并将 **执行** 字段设置为 *之后*，您将得到以下结果：

- 如果将 **按照更新的数量** 选项设置为 *是*，则会根据物料抽样中每个完成的数量和设置生成质检订单。 每次根据生产订单将数量完工入库时，都会根据新完成的数量生成新的质检订单。 此生成逻辑与采购一致。
- 如果将 **按照更新的数量** 选项设置为 *否*，则会根据完成的数量，在数量第一次完工入库时生成质检订单。 此外，根据物料抽样的跟踪维度，将基于剩余数量创建一个或多个质检订单。 后续的完成数量不会生成质检订单。

<table>
<thead>
<tr>
<th>质量规范</th>
<th>按照更新的数量</th>
<th>按照跟踪维度</th>
<th>结果</th>
</tr>
</thead>
<tbody>
<tr>
<td>百分比：10%</td>
<td>是</td>
<td>
<p>批处理号：否</p>
<p>序列号：否</p>
</td>
<td>
<p>订单数量：100</p>
<ol>
<li>30 的完工入库量
<ul>
<li>3 的质检订单 1（30 的 10%）</li>
</ul>
</li>
<li>70 的完工入库量
<ul>
<li>7 的质检订单 2（剩余订单数量的 10%，该数量在此例中为 70）</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>固定数量：1</td>
<td>否</td>
<td>
<p>批处理号：否</p>
<p>序列号：否</p>
</td>
<td>订单数量：100
<ol>
<li>30 的完工入库量
<ul>
<li>1 的质检订单 1（对于第一个完工入库数量，其固定值为 1）</li>
<li>1 的质检订单 2（对于剩余数量，其固定值仍为 1）</li>
</ul>
</li>
<li>10 的完工入库量
<ul>
<li>未创建质检订单。</li>
</ul>
</li>
<li>60 的完工入库量
<ul>
<li>未创建质检订单。</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>固定数量：1</td>
<td>是</td>
<td>
<p>批处理号：是</p>
<p>序列号：是</p>
</td>
<td>
<p>订单数量：10</p>
<ol>
<li>3 的完工入库量：批处理号 b1、序列号 s1 为 1；批处理号 b2、序列号 s2 为 1；批处理号 b3、序列号 s3 为 1
<ul>
<li>批处理号 b1、序列号 s1 为 1 的质检订单 1</li>
<li>批处理号 b2、序列号 s2 为 1 的质检订单 2</li>
<li>批处理号 b3、序列号 s3 为 1 的质检订单 3</li>
</ul>
</li>
<li>2 的完工入库量：批处理号 b4、序列号 s4 为 1；批处理号 b5、序列号 s5 为 1
<ul>
<li>批处理号 b4、序列号 s4 为 1 的质检订单 4</li>
<li>批处理号 b5、序列号 s5 为 1 的质检订单 5</li>
</ul>
</li>
</ol>
<p><strong>注意：</strong>批次可以重复使用。</p>
</td>
</tr>
<tr>
<td>固定数量：2</td>
<td>否</td>
<td>
<p>批处理号：是</p>
<p>序列号：是</p>
</td>
<td>
<p>订单数量：10</p>
<ol>
<li>4 的完工入库量：批处理号 b1、序列号 s1 为 1；批处理号 b2、序列号 s2 为 1；批处理号 b3、序列号 s3 为 1；批处理号 b4、序列号 s4 为 1
<ul>
<li>批处理号 b1、序列号 s1 为 1 的质检订单 1</li>
<li>批处理号 b2、序列号 s2 为 1 的质检订单 2</li>
<li>批处理号 b3、序列号 s3 为 1 的质检订单 3</li>
<li>批处理号 b4、序列号 s4 为 1 的质检订单 4</li>
</ul>
<ul>
<li>2 的质检订单 5，没有批处理号和序列号的引用</li>
</ul>
</li>
<li>6 的完工入库量：批处理号 b5、序列号 s5 为 1；批处理号 b6、序列号 s6 为 1；批处理号 b7、序列号 s7 为 1；批处理号 b8、序列号 s8 为 1；批处理号 b9、序列号 s9 为 1；批处理号 b10、序列号 s10 为 1
<ul>
<li>未创建质检订单。</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>其他资源

- [质量管理流程](quality-management-processes.md)
- [启用质量和不符合项管理](enable-quality-management.md)
- [仓库流程质量管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
