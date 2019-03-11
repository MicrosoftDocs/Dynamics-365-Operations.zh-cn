---
title: 质量管理概述
description: 本主题介绍如何在 Microsoft Dynamics 365 for Finance and Operations 中使用质量管理来帮助改进您的供应链中的产品质量。
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1630d13437d7e930fdf32ed5fdc61fc62bc33817
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "338306"
---
# <a name="quality-management-overview"></a>质量管理概述

[!include [banner](../includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 for Finance and Operations 中使用质量管理来帮助改进您的供应链中的产品质量。

质量管理可帮助您在处理未达标的产品时管理周转时间，而不管其源点如何。 因为诊断类型链接到更正报表，所以 Microsoft Dynamics 365 for Finance and Operations 可以计划任务以更正问题并防止重复执行它们。

除了管理不符合项的功能外，质量管理还包括按问题类型（甚至内部问题）跟踪问题以及将解决方案标识为短期或长期的功能。  有关关键绩效指标 (KPI) 的统计能让您了解以前的不符合项问题以及用于更正它们的解决方案的历史记录。 您可以使用历史数据检查以前质量度量的效果并确定相应的度量以备将来使用。

在您设置质量关联时，Finance and Operations 可以为各种业务流程、事件和条件生成质检订单。 质量关联可以包含特定物料、特定物料组或所有物料。

## <a name="examples-of-the-use-of-quality-management"></a>质量管理的使用示例
质量管理是可变的，并且可以以多种方式实施来满足特定级别供应链操作的要求。 以下示例说明对这些功能的可能用途：

-   根据预定义的标准自动启动质量控制流程（特定供应商的某一采购订单的仓库登记）。
-   在检查时锁定库存以防止使用未审核的库存（采购订单数量的完全锁定）。
-   使用物料抽样作为质量关联的一部分来定义必须检查的当前实际库存的金额。 抽样可以基于固定数量或百分比。
-   为部分收货创建质检订单。 若要创建基于某订单已实际接收的数量的质检订单，必须在**物料抽样**窗体上选择**按照更新的数量**复选框。
-   创建测试包括最小值、最大值和目标测试值在内的类型，然后执行具有预定义验证结果的定性与定量测试。
-   指定一个可接受质量级别 (AQL) 来控制质量度量容差。
-   指定检查操作所需的资源，如测试区域和测试仪器。

## <a name="working-with-quality-associations"></a>使用质量关联
使用质量关联的业务流程可与许多源文档相关，例如采购订单、销售订单或生产订单。

每个质量关联记录定义了测试组、AQL 和应用于生成的质检订单的抽样计划。 您必须为业务流程中每个变化形式定义质量关联记录。 例如，当更新采购订单产品收据时，您可以设置生成质检订单的质量关联。 根据执行计划的设置，在有未结质检订单或者下一流程（例如采购订单开票）时，可以将触发流程自身锁定。

**注释：** 在有未结质检订单时，会自动锁定库存数量使其不签发。 根据**物料抽样**页上的**完全锁定**设置，该数量是质检订单上的数量或源文档行上的数量。

对于给定业务流程，质量关联记录标识用于生成质检订单的事件和条件。 条件可以特定于站点或法人。 只有对于事件存在现有库存时，才能生成涉及破坏性测试的质检订单。

以下示例说明如何为各个业务流程中的变化形式定义质量关联记录。 对于每个示例，下表总结了质量关联记录定义的事件和条件。

<table>
<tbody>
<tr>
<th>引用类型</th>
<th>事件类型</th>
<th>执行</th>
<th>事件锁定</th>
<th>文档引用</th>
</tr>
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
<td rowspan="3">完工入库</td>
<td rowspan="2">之前</td>
<td>无</td>
<td rowspan="3">特定 ID、组或全部，以及资源特定、组或全部</td>
</tr>
<tr>
<td>完工入库</td>
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
<td rowspan="3">全部</td>
</tr>
<tr>
<td rowspan="2">完工入库</td>
<td>之前</td>
</tr>
<tr>
<td>之后</td>
</tr>
</tbody>
</table>

下表提供有关可以如何为特定类型的流程生成质检订单的详细信息。
<div class="tableSection">

<table>
<tbody>
<tr>
<th>流程的类型</th>
<th>可以自动生成质检订单时</th>
<th>需要破坏性测试的情况下可以生成质检订单时</th>
<th>条件信息</th>
<th>手动生成信息</th>
</tr>
<tr>
<td>采购订单</td>
<td>过帐收到的物料的收据清单或产品收据之前或之后</td>
<td>过帐收到的物料的产品收据之后，因为物料必须可用于破坏性测试</td>
<td>质检订单的需求可以反映特定的站点、物料或供应商，或者反映这些条件的组合。</td>
<td>引用某一采购订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</td>
</tr>
<tr>
<td>检验单</td>
<td>在检验单报告为已完工入库或已结束之前或之后</td>
<td>无法生成需要破坏性测试的质检订单。 假定检验单功能处理损坏物料的处置。</td>
<td>质检订单的需求可以反映特定的站点、物料或供应商，或者反映这些条件的组合。</td>
<td>引用某一检验单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</td>
</tr>
<tr>
<td>销售订单</td>
<td>在要被装运的物料的已计划领料流程或装箱单更新之前</td>
<td>任何步骤中</td>
<td>质检订单的需求可以反映特定的站点、物料或客户，或者反映这些条件的组合。</td>
<td>引用某一销售订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</td>
</tr>
<tr>
<td>生产订单</td>
<td>报告生产订单的完工数量之前或之后</td>
<td>报告生产订单的完工数量之后</td>
<td>质检订单的需求可以反映特定的站点或物料，或者反映这些条件的组合。</td>
<td>引用某一生产订单的手动生成的质检订单可以使用某一质量关联记录内的信息，例如测试抽样计划。</td>
</tr>
<tr>
<td>具有工艺路线工序的生产订单</td>
<td>在报告为已完成工序之前或之后</td>
<td>在报告生产最后一道工序完成后</td>
<td>质检订单的需求可以反映特定的站点、物料或运营资源，或者反映这些条件的组合。</td>
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

## <a name="quality-management-pages"></a>质量管理页
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>页面</th>
<th>描述</th>
<th>示例</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>质量关联</td>
<td>请参阅本文的前几部分。</td>
<td>质量关联定义生成的质检订单的所有以下信息：
<ul>
<li>交易记录事件</li>
<li>必须在物料上执行的测试组</li>
<li>AQL</li>
<li>抽样计划</li>
</ul>
您必须为业务流程中要求自动生成质检订单的每种变化定义质量关联。 例如，可以在业务流程中为采购订单、检验单、销售订单和生产订单生成质检订单。</td>
</tr>
<tr class="even">
<td>测试</td>
<td>使用此页可以定义和查看用于确定产品是否符合质量规范的各个测试。 您可以将一个或多个单独测试分配给测试组。 在这种情况下，您还可以指定测试特定信息，例如可接受的度量值。 度量值用于定量测试，测试变量用于定性测试。
<ul>
<li>定量测试具有测试类型<strong>整数</strong>或<strong>分数</strong>，并且具有指定的度量单位。 质量规范和测试结果表示为数字。</li>
<li>定性测试具有测试类型<strong>选项</strong>。 定性测试需要有关要度量的质量变量及其枚举选项的附加信息。 质量规范和测试结果根据结果表示。</li>
</ul></td>
<td>某个制造公司对采购物料执行两个测试：有关物料质量的定量测试和有关包装损坏的定性测试。 该公司定义有关质量测试的附加信息，以确定测试变量（损坏的包装）及其结果。 公司使用<strong>测试组</strong>页将两个测试分配给一个测试组并指定测试特定信息。 将测试组分配给质检订单，以便公司可以报告这两个测试的测试结果。</td>
</tr>
<tr class="odd">
<td>测试组</td>
<td>使用此页面可以设置、编辑和查看测试组以及分配给某个测试组的单独测试。 上部窗格显示测试组，而下部窗格显示分配给所选测试组的测试。 您可以向测试组分配多个策略，例如抽样计划、AQL 以及破坏性测试的要求。 当您将单个测试分配给测试组时，您需要定义其他信息，如顺序、文档和生效日期。 对于定量测试，还可以定义的信息包括可接受的度量值。 对于定性测试，该信息包括测试变量和默认结果。 分配给质检订单的测试组定义必须在特定物料上执行默认测试集。 但您可以添加、删除或更改质检订单上的测试。 将针对质检订单上的每个测试报告测试结果。</td>
<td>某制造公司为其质量准则的每个变化定义一个测试组。 多个测试组反映抽样计划中的差异、必须一起执行的测试集、AQL 和其他因素。 对于定量测试，可接受的度量值中也存在差别。 为了落实其质量准则，公司在<strong>质量关联</strong>页上将一个测试组分配给用于自动生成质检订单的每个规则，而且还将一个测试组分配给手动创建的质检订单。</td>
</tr>
<tr class="even">
<td>物料质量组</td>
<td>使用此页面可以设置、编辑和查看分配给质量组的物料或分配给物料的质量组。 质量组表示物料的公共测试要求。 在<strong>测试组</strong>页上定义测试要求后，您可以定义用于自动生成质检订单的规则。 为了简化该流程，您不为各个物料定义规则。 相反，您使用<strong>质量关联</strong>页为质量组定义规则。 您还可以为所选质量组使用<strong>物料质量组</strong>页来将相关物料分配给该组。 您还可以为所选物料使用<strong>物料质量组</strong>页来将相关质量组分配给该物料。</td>
<td>某制造公司采购的多种原材料具有相同的进货检查测试要求。 公司定义了一个质量组，然后将与原材料关联的物料编号分配给该组。 之后，公司采购一个新类型的原材料，具有相同的测试要求。 公司不是为新物料设置新的测试要求，而是将新物料的物料编号添加到现有的质量组。 此相同制造公司还生产具有相同测试要求的物料，并装运具有相同装运前测试要求的物料。 公司定义两个附加质量组，然后将相关物料编号分配给每个组。</td>
</tr>
<tr class="odd">
<td>测试变量</td>
<td>使用此页可以定义和查看与定性测试关联的变量。 对于每个变量，您定义表示可能选项的枚举结果。 您在<strong>测试</strong>页上定义测试。 对于定性测试，您必须将测试类型设置为<strong>选项</strong>。 使用<strong>测试组</strong>页可以将测试变量分配给单个测试。</td>
<td>一个生产饼干的制造公司对成品使用检查测试。 此检查测试具有多个变量。 一个变量是味道，并且此变量的可能结果是好和坏。 第二个变量是颜色，其可能结果是过暗、过浅和正好。</td>
</tr>
<tr class="even">
<td>测试变量结果</td>
<td>使用此页面可以设置、编辑和查看与定性测试关联的测试变量的可能测试结果。 对于每个结果，您分配<strong>通过</strong>或<strong>未通过</strong>状态。 您必须在<strong>测试</strong>页上定义的每个定性测试定义变量及其结果。 （对于定性测试，测试类型在<strong>测试</strong>页上设置为<strong>选项</strong>。）使用<strong>测试组</strong>页可以将测试变量和默认结果分配给单独的定性测试。</td>
<td>一个生产饼干的制造公司对成品使用检查测试。 此检查测试具有多个变量。 一个变量是味道，并且此变量的可能结果是好和坏。 第二个变量是颜色，其可能结果是过暗、过浅和正好。 会为每个结果分配一个<strong>通过</strong>或<strong>未通过</strong>的状态。 在各个变量的检查测试期间，检查员将通过选择其中一个结果报告测试结果。</td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>其他资源
--------

[质量管理流程](quality-management-processes.md)

[启用未达标管理](enable-nonconformance-management.md)
