---
title: 交货备选方案
description: 销售订单处理人员可以使用交货备选方案页发现备选订单履行选项。
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 48cc8974cc8a8769b3d05f47f82166164e877ae5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423041"
---
# <a name="delivery-alternatives"></a>交货备选方案

[!include [banner](../includes/banner.md)]

销售订单处理人员可以使用 **交货备选方案** 页发现备选订单履行选项。

**交货备选方案** 页面布局提供所有备选方案的概览。 它还能让订单处理人员在当前公司以外寻找履行机会。 他们现在可以查看内部公司机会和来自外部供应商的机会。 通过按交货日期排序选项，销售订单处理人员可以查看交货备选方案的智能列表。 此外，参数帮助他们更好地管理建议的交货。 因为运输时间可以影响交货日期，销售订单处理人员可以探索承运人提供的各种运输选择。 由于详细信息为每个建议显示，订单处理人员可以直接从 **交货备选方案** 页做出明智的决定。

## <a name="open-the-delivery-alternatives-page"></a>打开“交货备选方案”页
您可以从销售订单行打开 **交货备选方案** 页。

1.  单击 **产品和供应**&gt;**交货备选方案**。
2.  单击 **行明细**&gt;**交货**&gt;**交货备选方案**。

您还可以通过打开 **销售订单处理和查询** 工作区打开 **交货备选方案** 页，然后单击 **订单和收藏**&gt;**延迟的订单行**&gt;**交货备选方案** **注意：** 只有当同时满足以下两个条件时，您才能够打开 **交货备选方案** 页：

-   所有必需销售订单行信息均已填写。
-   **交货日期控制** 字段设置为 **无** 以外的值。

## <a name="delivery-date-control-methods"></a>交货日期控制方法
交货日期控制方法确定系统如何确定交货日期，如何计算交货备选方案，以及显示哪些信息。 请注意，交货数据控制考虑日历。 因此，以下日历可能影响建议的收货日期：仓库日历、运输日历、供应商日历和客户日历。 下表描述交货日期控制的各个方法。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>方法</strong></td>
<td><strong>说明</strong></td>
</tr>
<tr class="even">
<td><strong>无</strong></td>
<td><ul>
<li>不支持销售订单行的交货备选方案。 此选项关闭交货数据控制。</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>销售提前期</strong></td>
<td><ul>
<li>交货备选方案根据预定义的销售提前期计算。 运输天数基于交货方式计算。</li>
<li>交货备选方案包括具有现有库存量库存和供应/需求订单的仓库。</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ATP</strong></td>
<td><ul>
<li>交货备选方案根据可承诺 (ATP) 逻辑计算。 考虑当前可用性以及预期的将来可用性。 运输天数基于交货方式计算。</li>
<li>交货备选方案包括具有现有库存量库存和供应/需求订单的仓库。</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>ATP + 发货宽限期</strong></td>
<td><ul>
<li>交货备选方案针对 ATP 方法计算，但是，发货宽限期包括在计算中。</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>CTP</strong></td>
<td><ul>
<li>交货备选方案根据可承诺量 (CTP) 逻辑计算。 MRP 分解用于确定可用性。 请注意，CTP 至少将交货日期偏移至销售提前期。 运输天数基于交货方式计算。</li>
<li>交货备选方案包括以下仓库的建议：
<ul>
<li>当前仓库</li>
<li>默认仓库</li>
<li>具有现有库存量的所有仓库</li>
<li>具有供应订单的所有仓库</li>
<li>具有有效物料清单 (BOM) 版本的所有仓库</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a>查看有关交货备选方案的信息
此节介绍在 **交货备选方案** 页的每个选项卡上可用的交货备选方案的信息。

### <a name="products"></a>产品

此选项卡显示当前销售订单行的产品和详细信息的汇总。

### <a name="delivery-alternatives"></a>交货备选方案

此选项卡显示按收货数据排序的交货备选方案的列表。 在列表上，您可以选择建议所基于的选项。 您还可以选择某一交货方式，确定运输天数。 选项如下：

-   **包括其他产品变型** - 此选项对于包含产品变型的产品可用。 它将包括其他产品变型的交货备选方案。 此选项对 CTP 不可用。
-   **包括部分数量** - 默认情况下，仅包括执行销售订单行的完整数量的建议。 选择此选项可以包含行只部分执行订单的建议。 当客户请求更早的交货日期并接受部分交货时，此选项很有用。
-   **包括更晚的日期** - 默认情况下，只显示好于（早于）销售订单行上的当前日期的建议。 选择此选项以包括更晚的日期。 此选项在日期之外的参数具有优先级的情况下很有用。 例如，特定供应商或仓库可能是首选。
-   **交货方式** - 选择首选交货方式来优化运输时间和成本。 您将立即看到建议的交货备选方案的效果。 因此，比较备选方案更轻松。
-   **包括采购** - 在选择采购时，建议的交货备选方案包括从外部供应商和企业（内部公司）的其他公司采购的选项。 **包括采购** 选项支持 ATP 和 ATP + 发货宽限期交货日期控制。 来自产品默认供采购应商以及产品所有已审核供应商的采购选项都将包括在内。
-   对于外部供应商，计算基于采购提前期。
-   对于内部公司，计算考虑采购公司的可用量，基于采购公司的交货日期控制。
-   **交货类型**（与采购相关）
    -   **存货** - 产品从采购仓库装运到销售订单行的站点/仓库。 然后从该仓库装运到客户。
    -   **直接交运** - 产品直接从采购仓库装运给客户。

### <a name="availability-information"></a>可用信息

此选项卡上的信息与所选交货备选方案行相关。 以下信息根据销售订单行的交货日期控制显示：

-   **销售提前期**
    -   **今天可用** - 显示当前实际现有量、实际预留和实际可用库存。
    -   **参数** - 显示库存单位和销售提前期。

-   **ATP and ATP + 发货宽限期**
    -   **今天可用** - 显示当前实际现有量、实际预留和实际可用库存。
    -   **参数** - 显示库存单位和销售提前期。
    -   **将来的可用性** - 显示 **交货备选方案** 下所选站点和仓库的当前和未来可用性的图形表示形式。 您可单击图表列查看有关产品的将来可用性的更多详细信息。 此滑块显示 ATP 时限内相关需求和供应订单的列表。

-   **CTP**
    -   **今天可用** - 显示当前实际现有量、实际预留和实际可用库存。
    -   **参数** - 显示库存单位和销售提前期。
    -   **分解** - 显示所选交货备选方案的供应分解。 您可以使用 **设置** 更改在分解中显示的字段和库存维度。

### <a name="impact-of-selected-alternative"></a>选定替换的影响

此选项卡突出显示所选交货备选方案的影响。 如果您单击 **确定**，销售订单行更新为所选列中突出显示的值。 请注意，如果所选交货备选方案的数量少于销售订单行的数量，将创建交货计划，并且销售订单行拆分为两行：一行为选择的数量，一行为剩余数量。 您还可以更新业务行，以便其与计划行匹配并影响定价。

<a name="additional-resources"></a>其他资源
--------

[订单承诺](delivery-dates-available-promise-calculations.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]